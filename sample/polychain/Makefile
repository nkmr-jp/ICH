BUILD_DIR=./build

#See: https://www.youtube.com/watch?v=jd0lnLyluXE&t=763s
build-chaincode-fabric:
	mkdir -p $(BUILD_DIR)
	mkdir -p $(BUILD_DIR)/fabric
	mkdir -p $(BUILD_DIR)/fabric/hellopoly

	cp ./fabric-contract/testnet/hellopoly/cmd/main.go $(BUILD_DIR)/fabric/
	cp ./fabric-contract/testnet/hellopoly/chaincode.go $(BUILD_DIR)/fabric/hellopoly/
	cd $(BUILD_DIR)/fabric/; zip hellopoly.zip main.go hellopoly/*

build-chaincode-fisco:
	mkdir -p $(BUILD_DIR)
	mkdir -p $(BUILD_DIR)/fisco
	mkdir -p $(BUILD_DIR)/fisco/hellopoly

	cp ./fisco_contracts/hellopoly/IEthCrossChainManager.sol $(BUILD_DIR)/fisco/hellopoly/
	cp ./fisco_contracts/hellopoly/IEthCrossChainManagerProxy.sol $(BUILD_DIR)/fisco/hellopoly/
	cp ./fisco_contracts/hellopoly/PolyFabricToFisco2.sol $(BUILD_DIR)/fisco/hellopoly/
	cd $(BUILD_DIR)/fisco/hellopoly/; zip hellopoly.zip IEthCrossChainManager.sol IEthCrossChainManagerProxy.sol PolyFabricToFisco2.sol