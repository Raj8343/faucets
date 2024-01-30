# faucets
import { TatumSDK, Network, Ethereum } from '@tatumio/tatum'

const tatum = await TatumSDK.init<Ethereum>({
  network: Network.ETHEREUM_HOLESKY,
  apiKey: {
    v4: 't-6509****07aed3',
  },
});

const res = await tatum.faucet.fund('0x712e3a792c974b3e3dbe41229ad4290791c75a82')

if (res.data) {
  console.log(res.data)
} else {
  console.error(res.error)
}
