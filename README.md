# What is SubQuery?

SubQuery powers the next generation of Polkadot dApps by allowing developers to extract, transform and query blockchain data in real time using GraphQL. In addition to this, SubQuery provides production quality hosting infrastructure to run these projects in.

# SubQuery Example - Simple Aggregation

This very basic SubQuery indexes staked rewards and determines the total rewards for each account, demonstrating how to aggregate data. 
 
# Getting Started

### 1. Clone the entire subql-example repository

```shell
git clone https://github.com/subquery/tutorials-simple-aggregation.git

```
### 2. Install dependencies

```shell
cd tutorials-simple-aggregation
# Yarn
yarn

#NPM
npm install
```

### 3. Generate types

```shell
#Yarn
yarn codegen

#NPM
npm run-script codegen
```

### 4. Build the project

```shell
#Yarn
yarn build

#NPM
npm run-script build
```

### 5. Run locally

```shell
#Yarn
yarn start:docker

#NPM
npm run start:docker
```
### 6. Example queries to run
```shell
query{
  sumRewards(first:10){
    nodes{
      id
      accountReward
      createdAt
      blockheight
    }
  }
}
```
