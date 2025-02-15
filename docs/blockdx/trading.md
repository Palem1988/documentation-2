title: Block DX Trading Guide
description: These Block DX trading guides explain how to check your balances, select your market, make orders, take orders, check order status, and view order history.


# Block DX Trading
[Block DX](/blockdx/introduction) is the fastest, most secure, most reliable, and most decentralized exchange (DEX), built on the [Blocknet Protocol](/project/introduction). Follow the guides below to learn how to check your balances, select your market, make orders, take orders, check order status, and view order history. If Block DX has not been setup yet, please follow the [setup guide](/blockdx/setup).

<iframe width="560" height="315" src="https://www.youtube.com/embed/6QcyazmnXws?start=214" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

??? example "Balances"
	The first thing you want to do when starting Block DX is to check your balances. *Balances* displays the connected wallets along with the *available* balance. A connected wallet is one that has been configured and is currently open and unlocked. The *available* balance is the balance of the funds in a wallet that are not locked up.

	![Balances](/img/blockdx/balances-unequal.png)

	The *Available* balance may show a value different than what's displayed in the wallet if:

	* The wallet is locked.
	* You have already made a trade that has locked up funds. You will want to create smaller inputs so that a single trade won't lock up more funds than needed.
	* Funds aren't in a legacy address. Right now only legacy addresses are compatible. If you are using a Segwit address, please create a new address to send the funds to. If the wallet has been configured via Block DX, then a legacy address will automatically be created when generating a new address.
	* The wallet was not [configured](/blockdx/configuration).
	* The wallet was not restarted after the configuration.
	* If inputs have been locked via Coin Control.


??? example "Select Market"
	1. The market selection tool can be found in the upper-left corned.

		![Select Market](/img/blockdx/select-market-1.png)

	1. Click the *Select market pair* button.
	1. A downdown will appear with two lists: the assets of the wallets you have connected and all assets listed on Block DX.

		![Select Market](/img/blockdx/select-market-2.png)

	1. From *Connected Tokens*, select the asset you would like to trade.
	1. Select the asset you would like to trade the first asset with. The first asset will be priced in terms of this asset. This asset must have a wallet configured.

		![Select Market](/img/blockdx/select-market-3.png)

	1. Select *Select* to view the chosen market.
		
		![Select Market](/img/blockdx/select-market-4.png)


??? example "Market Information"
	Each market has a price chart, depth chart, and market stats available.

	![Market Data](/img/blockdx/market-data.png)

	The market stats are above the price chart and show the last trade price, percent in price change over the last 24 hour rolling period, and volume over the last 24 hour rolling period.

	![Stats](/img/blockdx/navbar-stats.png)

	The chart has the ability to zoom. To zoom in, click and drag the pointer over the are you want to zoom in on.

	![Price Chart Zoom](/img/blockdx/price-chart-zoom.png)

	You can hover over the candles to show the information of each data point in the legend.

	![Price Chart Zoomed](/img/blockdx/price-chart-zoomed.png)

	To reset the chart, select the *Show All* button in the upper-right corner of the chart.

	![Show All](/img/blockdx/price-chart-show-all.png)

	To the right of the price chart there's also a depth chart. The depth chart shows how much market depth there is of orders at certain prices.

	![Depth Chart](/img/blockdx/depth-chart.png)

	Hover order the depth chart to view the data values.

	![Depth Chart Hover](/img/blockdx/depth-chart-hover.png)


??? example "Make Order"
	
	![Make Order](/img/blockdx/make-order.png)

	1. Review the [trading fees](/blockdx/fees/#maker-fee) for making orders.
	1. At the left side of Block DX you will find an order form.
	1. Select either the buy or sell tab.
	1. For *Amount* (the first input), enter the amount you would like to buy or sell.

		??? info "Note: There are no limit, market, or partial orders."
			At the moment there are just *Exact* orders, meaning that orders must be taken for the exact amounts. Due to this setup, if trading a large amount it may be best to instead break the order into a few smaller separate orders.

	1. For *Price* (the second input), enter the price (rate) you would like to trade the first asset for.
	1. *Total* shows the total amount of the 2nd asset that will be traded for the first asset.
	1. In the address inputs, enter the addresses the funds will be coming from and going to. Make sure these are legacy addresses and not Segwit addresses.

		??? bug "Bug: Right-click paste does not work properly."
			When pasting, use the Ctrl+v shortcut. Using right-click and paste will not be recorded in the input even though it's showing.

	1. Ignore *Order ID*, that should be blank when creating an order.
	1. Review your order.
	1. Select the place order button.
	1. The trade will now be visible as *Open* under *Active Orders*.

		![Active](/img/blockdx/orders-active.png)

	The Blocknet wallet and the wallets that are being traded out of must remain open and unlocked during trading. If the Blocknet wallet is closed, any open orders will automatically be cancelled.


??? example "Take Order"
	1. Review the [trading fees](/blockdx/fees/#taker-fee) for taking orders.
	1. On the right side of Block DX you will find the order book.
		![Order Book](/img/blockdx/order-book.png)
	1. Click on the order you would like to take.

		??? info "Note: There are no limit, market, or partial orders."
			At the moment there are just *Exact* orders, meaning that orders must be taken for the exact amounts. Due to this setup, you must have enough funds to cover the entire sell amount of the order selected.

	1. The order form on the left side of Block DX will auto-populate.

		![Take Order](/img/blockdx/take-order.png)

	1. Make sure *Balances* shows enough funds in the *Available* column to cover the order.
	1. In the address inputs, enter the addresses the funds will be coming from and going to. Make sure these are legacy addresses and not Segwit addresses.

		??? bug "Bug: Right-click paste does not work properly."
			When pasting, use the Ctrl+v shortcut. Using right-click and paste will not be recorded in the input even though it's showing.

	1. Review your order.
	1. Select the place order button.
	1. The trade will now be visible under *Active Orders*.
	1. The trade should complete in about 20-30 seconds.

	The Blocknet wallet and the wallets that are being traded out of must remain open and unlocked during trading. If the Blocknet wallet is closed, any open orders will automatically be cancelled.


??? example "Order Status"
	Any orders that are open or in progress can be found in *Active Orders*.

	![Active](/img/blockdx/orders-active.png)

	You can hover over the order to read the order state.

	![Active](/img/blockdx/orders-active-open.png)

	Any orders that are cancelled, completed, or failed can be found in *Inactive Orders*

	![Inactive](/img/blockdx/orders-inactive.png)

	Again, you can hover over the order to read the order state. There are different icons to represent each order state.

	![Inactive Complete](/img/blockdx/orders-inactive-complete.png)
	![Inactive Cancelled](/img/blockdx/orders-inactive-cancelled.png)

	If you have created an order, it will be indicated in the order book with a white dot.

	![Order Book](/img/blockdx/order-book-own-order.png)

	The Blocknet wallet and the wallets that are being traded out of must remain open and unlocked during trading. If the Blocknet wallet is closed, any open orders will automatically be cancelled.


??? example "Order History"
	At the bottom-right corner of Block DX you can find the trade history. The trade history information is gathered only for the wallets that are configured. Therefore, the trade history will only show the orders that have been completed since Blocknet wallet and wallets for the currently viewed market have been opened and unlocked. If the Blocknet wallet is restarted, this information will be cleared and no longer visible.

	![Trade History](/img/blockdx/trade-history.png)











<script type="text/javascript">
// read instructions for related links in ../snippets/extras.md
var relatedLinks = [];
</script>

--8<-- "extras.md"





