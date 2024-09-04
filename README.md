# ABI-hackathon-lagos

```js
const ABI_ZKSYNC = [
  { inputs: [{ internalType: "address", name: "_gameVaultToken", type: "address" }], stateMutability: "nonpayable", type: "constructor" },
  { inputs: [], name: "ExceededFundingGoal", type: "error" },
  { inputs: [], name: "InsufficientInput", type: "error" },
  { inputs: [], name: "InvalidProposal", type: "error" },
  { inputs: [], name: "NoVotingPower", type: "error" },
  { inputs: [], name: "NotActive", type: "error" },
  { inputs: [], name: "NotActiveCause", type: "error" },
  { inputs: [], name: "NotInDuration", type: "error" },
  { inputs: [], name: "NotOwner", type: "error" },
  { inputs: [], name: "TimeNotReached", type: "error" },
  {
    anonymous: false,
    inputs: [
      { indexed: true, internalType: "uint256", name: "_ID", type: "uint256" },
      { indexed: false, internalType: "uint256", name: "_fundingBalance", type: "uint256" },
      { indexed: false, internalType: "address", name: "contributor", type: "address" },
      { indexed: false, internalType: "uint256", name: "amount", type: "uint256" },
    ],
    name: "ContributeEth",
    type: "event",
  },
  {
    anonymous: false,
    inputs: [
      { indexed: false, internalType: "uint256", name: "id", type: "uint256" },
      { indexed: false, internalType: "string", name: "_title", type: "string" },
      { indexed: false, internalType: "uint256", name: "_fundingGoal", type: "uint256" },
      { indexed: false, internalType: "uint256", name: "_durationTime", type: "uint256" },
    ],
    name: "CreateGofundme",
    type: "event",
  },
  {
    anonymous: false,
    inputs: [
      { indexed: true, internalType: "uint256", name: "_ID", type: "uint256" },
      { indexed: false, internalType: "bool", name: "isActive", type: "bool" },
    ],
    name: "GetContributedFunds",
    type: "event",
  },
  {
    anonymous: false,
    inputs: [
      { indexed: true, internalType: "uint256", name: "_ID", type: "uint256" },
      { indexed: false, internalType: "bytes32", name: "proposal", type: "bytes32" },
    ],
    name: "ProposalCreated",
    type: "event",
  },
  {
    anonymous: false,
    inputs: [
      { indexed: true, internalType: "address", name: "recipient", type: "address" },
      { indexed: false, internalType: "uint256", name: "points", type: "uint256" },
      { indexed: false, internalType: "uint256", name: "tokenAmount", type: "uint256" },
    ],
    name: "TokensTransferred",
    type: "event",
  },
  {
    anonymous: false,
    inputs: [
      { indexed: true, internalType: "uint256", name: "_ID", type: "uint256" },
      { indexed: false, internalType: "bytes32", name: "proposal", type: "bytes32" },
      { indexed: false, internalType: "uint256", name: "votingPower", type: "uint256" },
    ],
    name: "VoteCast",
    type: "event",
  },
  {
    inputs: [{ internalType: "uint256", name: "", type: "uint256" }],
    name: "activeCampaignsIds",
    outputs: [{ internalType: "uint256", name: "", type: "uint256" }],
    stateMutability: "view",
    type: "function",
  },
  {
    inputs: [
      { internalType: "uint256", name: "", type: "uint256" },
      { internalType: "address", name: "", type: "address" },
    ],
    name: "contribute",
    outputs: [{ internalType: "uint256", name: "", type: "uint256" }],
    stateMutability: "view",
    type: "function",
  },
  { inputs: [{ internalType: "uint256", name: "_ID", type: "uint256" }], name: "contributeEth", outputs: [], stateMutability: "payable", type: "function" },
  {
    inputs: [
      { internalType: "address", name: "", type: "address" },
      { internalType: "uint256", name: "", type: "uint256" },
    ],
    name: "contributors_",
    outputs: [
      { internalType: "address", name: "contributor", type: "address" },
      { internalType: "uint256", name: "balance", type: "uint256" },
      { internalType: "uint256", name: "time", type: "uint256" },
    ],
    stateMutability: "view",
    type: "function",
  },
  {
    inputs: [
      { internalType: "address", name: "player", type: "address" },
      { internalType: "uint256", name: "points", type: "uint256" },
    ],
    name: "convertPointandTransfer",
    outputs: [],
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    inputs: [
      { internalType: "address", name: "creator", type: "address" },
      { internalType: "string", name: "_title", type: "string" },
      { internalType: "string", name: "_description", type: "string" },
      { internalType: "uint256", name: "_fundingGoal", type: "uint256" },
      { internalType: "uint256", name: "_durationTime", type: "uint256" },
    ],
    name: "createGofundme",
    outputs: [{ internalType: "uint256", name: "_id", type: "uint256" }],
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    inputs: [
      { internalType: "uint256", name: "_ID", type: "uint256" },
      { internalType: "bytes32", name: "proposal", type: "bytes32" },
    ],
    name: "createProposal",
    outputs: [],
    stateMutability: "nonpayable",
    type: "function",
  },
  { inputs: [], name: "denum", outputs: [{ internalType: "uint256", name: "", type: "uint256" }], stateMutability: "view", type: "function" },
  {
    inputs: [{ internalType: "uint256", name: "", type: "uint256" }],
    name: "funder",
    outputs: [
      { internalType: "uint256", name: "id_", type: "uint256" },
      { internalType: "string", name: "title", type: "string" },
      { internalType: "string", name: "description", type: "string" },
      { internalType: "uint256", name: "fundingGoal", type: "uint256" },
      { internalType: "address", name: "owner", type: "address" },
      { internalType: "uint256", name: "startTime", type: "uint256" },
      { internalType: "uint256", name: "durationTime", type: "uint256" },
      { internalType: "bool", name: "isActive", type: "bool" },
      { internalType: "uint256", name: "fundingBalance", type: "uint256" },
    ],
    stateMutability: "view",
    type: "function",
  },
  { inputs: [], name: "getAllCampaignsCount", outputs: [{ internalType: "uint256", name: "", type: "uint256" }], stateMutability: "view", type: "function" },
  { inputs: [], name: "getCampaigns", outputs: [{ internalType: "uint256[]", name: "", type: "uint256[]" }], stateMutability: "view", type: "function" },
  { inputs: [{ internalType: "uint256", name: "_ID", type: "uint256" }], name: "getContributedFunds", outputs: [], stateMutability: "nonpayable", type: "function" },
  {
    inputs: [{ internalType: "uint256", name: "_ID", type: "uint256" }],
    name: "getContributors",
    outputs: [
      {
        components: [
          { internalType: "address", name: "contributor", type: "address" },
          { internalType: "uint256", name: "balance", type: "uint256" },
          { internalType: "uint256", name: "time", type: "uint256" },
        ],
        internalType: "struct Contributors[]",
        name: "_contributors",
        type: "tuple[]",
      },
    ],
    stateMutability: "view",
    type: "function",
  },
  { inputs: [{ internalType: "uint256", name: "_ID", type: "uint256" }], name: "getStatus", outputs: [{ internalType: "bool", name: "", type: "bool" }], stateMutability: "view", type: "function" },
  {
    inputs: [
      { internalType: "uint256", name: "", type: "uint256" },
      { internalType: "address", name: "", type: "address" },
    ],
    name: "hasContributed",
    outputs: [{ internalType: "bool", name: "", type: "bool" }],
    stateMutability: "view",
    type: "function",
  },
  { inputs: [], name: "id", outputs: [{ internalType: "uint256", name: "", type: "uint256" }], stateMutability: "view", type: "function" },
  { inputs: [], name: "num", outputs: [{ internalType: "uint256", name: "", type: "uint256" }], stateMutability: "view", type: "function" },
  { inputs: [{ internalType: "uint256", name: "newNum", type: "uint256" }], name: "updateNum", outputs: [], stateMutability: "nonpayable", type: "function" },
  {
    inputs: [
      { internalType: "uint256", name: "_ID", type: "uint256" },
      { internalType: "bytes32", name: "proposal", type: "bytes32" },
    ],
    name: "voteOnProposal",
    outputs: [],
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    inputs: [
      { internalType: "uint256", name: "", type: "uint256" },
      { internalType: "address", name: "", type: "address" },
    ],
    name: "votingPower",
    outputs: [{ internalType: "uint256", name: "", type: "uint256" }],
    stateMutability: "view",
    type: "function",
  },
];

export default ABI_ZKSYNC;

```
