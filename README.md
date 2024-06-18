# Aligned-Layer

![340602794-e8c0f6fc-866e-4934-9173-5a0770b533ea](https://github.com/0xtuncay/Aligned-Layer/assets/126924328/f2618ec7-9762-43ed-882d-473a1598b54d)


| Bileşenler | Minimum Gereksinimler | 
| ------------ | ------------ |
| Ubuntu 22, ve üstü |
| CPU |	 |
| RAM	|  GB |
| Storage	|  GB SSD |

# Sending and Verifying SP1 Proofs with Aligned

#Alignedi indiriyoruz.

```
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/install_aligned.sh | bash
```

```
source /root/.bashrc
```

# Örnek Sp1 Prof Dosyasını indiriyoruz.

```
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/get_proof_test_files.sh | bash
```

# Proof'u Gönderiyoruz.

```
aligned submit \
  --proving_system SP1 \
  --proof ~/.aligned/test_files/sp1_fibonacci.proof \
  --vm_program ~/.aligned/test_files/sp1_fibonacci-elf \
  --aligned_verification_data_path ~/aligned_verification_data \
  --conn wss://batcher.alignedlayer.com
```

#  Proof'u On-Chain'de Doğruluyoruz.

```
aligned verify-proof-onchain \
  --aligned-verification-data ~/aligned_verification_data/*.json \
  --rpc https://ethereum-holesky-rpc.publicnode.com \
  --chain holesky
```

En Son Size Explorerli Bir bağlantı verecek, Onunla birlikte bir tweet atıyoruz. Ve tweet Linkini, discorddan, testnet bölümüne atıyoruz.
Ve aligned_verification_data klasörünün içindeki dosyayı kaydediyoruz.




