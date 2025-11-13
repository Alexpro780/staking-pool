Short description (EN): A minimal pooled staking contract where users deposit ETH and track their share of the total stake.
def main() -> None:
    args = parse_args()

    if args.show_log:
        log = load_log()
        print(summarize_log(log))
        return

    if not (args.network and args.obj_type and args.value):
        interactive_mode()
        return
