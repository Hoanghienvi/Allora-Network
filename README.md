# Allora Network
<p align="center">
<img src='assets/AlloraLogo.jpeg' width='200'>
<a href="https://goreportcard.com/badge/github.com/allora-network/allora-chain">
    <img src="https://goreportcard.com/badge/github.com/allora-network/allora-chain">
</a>
</p>

![Docker!](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Go!](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Apache License](https://img.shields.io/badge/Apache%20License-D22128?style=for-the-badge&logo=Apache&logoColor=white)

The Allora Network is a state-of-the-art protocol that uses decentralized AI and machine learning (ML) to build, extract, and deploy predictions among its participants. It offers actors who wish to use AI predictions a formalized way to obtain the output of state-of-the-art ML models on-chain and to pay the operators of AI/ML nodes who create these predictions. That way, Allora bridges the information gap between data owners, data processors, AI/ML predictors, market analysts, and the end-users or consumers who have the means to execute on these insights.

The AI/ML agents within the Allora Network use their data and algorithms to broadcast their predictions across a peer-to-peer network, and they ingest these predictions to assess the predictions from all other agents. The network consensus mechanism combines these predictions and assessments, and distributes rewards to the agents according to the quality of their predictions and assessments. This carefully designed incentive mechanism enables Allora to continually learn and improve, adjusting to the market as it evolves.

### Documentation
For the latest documentation, please go to https://docs.allora.network/

Úng hộ Ref: https://app.allora.network?ref=eyJyZWZlcnJlcl9pZCI6IjQ2MGEwZmQ4LTZmNWMtNDQxMi05M2Y4LWQ5MjU4ZmQ0ZTNkNCJ9

## Cấu hình yêu cầu chạy node
```
Operating System : Ubuntu 22.04
CPU : Minimum of 1/2 core
RAM : 2 to 4 GB
Storage : SSD or NVMe with at least 5GB of space
```

## Create Wallet & Request Faucet

Code auto sẽ tự tạo ví mới sau đó copy Contract đến web faucet token
```
https://faucet.edgenet.allora.network/
```
## Lệnh Auto chạy Node với 1 Lệnh
Note: Nhớ lưu lại Mã khôi phục Ví
```
wget https://raw.githubusercontent.com/Hoanghienvi/Allora-Network/main/autocode.sh && chmod +x autocode.sh && ./autocode.sh
```
## Sau khi cài đặt hoàn tất check lại node
```
  curl --location 'http://localhost:6000/api/v1/functions/execute' \
--header 'Content-Type: application/json' \
--data '{
    "function_id": "bafybeigpiwl3o73zvvl6dxdqu7zqcub5mhg65jiky2xqb4rdhfmikswzqm",
    "method": "allora-inference-function.wasm",
    "parameters": null,
    "topic": "1",
    "config": {
        "env_vars": [
            {
                "name": "BLS_REQUEST_PATH",
                "value": "/api"
            },
            {
                "name": "ALLORA_ARG_PARAMS",
                "value": "ETH"
            }
        ],
        "number_of_nodes": -1,
        "timeout": 2
    }
}'
```
## Chờ Kết quả.
```
{"code":"200","request_id":"876a58bf-2cad-49ff-a722-86a5da444528","results":[{"result":{"stdout":"{\"infererValue\": \"2908.09263675852\"}\n\n","stderr":"","exit_code":0},"peers":["12D3KooWM99J9Qc9QhsBXiezdJKr9Y6MJN3LDL8XfcBDbCn1qtAp"],"frequency":100}],"cluster":{"peers":["12D3KooWM99J9Qc9QhsBXiezdJKr9Y6MJN3LDL8XfcBDbCn1qtAp"]}}
```
