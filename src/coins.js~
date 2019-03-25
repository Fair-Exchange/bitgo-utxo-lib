// Coins supported by bitgo-bitcoinjs-lib
const typeforce = require('typeforce')

const coins = {
  BCH: 'bch',
  BTC: 'btc',
  BTG: 'btg',
  LTC: 'ltc',
  ZEC: 'zec',
  SAFECOIN: 'safecoin',
  SAFECOINTEST: 'safecointest',
  DASH: 'dash',
  DEFAULT: 'default'
}

coins.isBitcoin = function (network) {
  return typeforce.value(coins.BTC)(network.coin)
}

coins.isBitcoinCash = function (network) {
  return typeforce.value(coins.BCH)(network.coin)
}

coins.isBitcoinGold = function (network) {
  return typeforce.value(coins.BTG)(network.coin)
}

coins.isLitecoin = function (network) {
  return typeforce.value(coins.LTC)(network.coin)
}

coins.isZcash = function (network) {
  return !!network.isZcash
}

coins.isSafecoin = function (network) {
  return typeforce.value(coins.SAFECOIN)(network.coin)
}

coins.isValidCoin = typeforce.oneOf(
  coins.isBitcoin,
  coins.isBitcoinCash,
  coins.isBitcoinGold,
  coins.isLitecoin,
  coins.isZcash
)

module.exports = coins
