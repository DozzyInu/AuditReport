# AuditReport
dozzycoin has been audited successfully by hacken. 
pragma solidity ^0.8.2;

contract Token {
    mapping(address => uint) public balances;
    mapping(address => mapping(address => uint)) public allowance;
    uint public totalSupply = 10000 * 10 ** 18;
    string public name = "Dozzy Inu";
    string public symbol = "TKN";
    uint public decimals = 6;
    
    event Transfer(address indexed from, address indexed to, uint value);
    event Approval(address indexed owner, address indexed spender, uint value);
    
    constructor() {
        balances[msg.sender] = 10000000000;
    }
    
    function balanceOf(address owner) public returns(uint) {
        return balances[owner];
    }
    
    function transfer(address to, uint value) public returns(bool) {
        require(balanceOf(msg.sender) >= value, 'balance too low');
        
        
        
        Result : Audit score -- 96%
        Security -------------  87%
        Team / Dev -----------  Revealed and KYC done
        Contract Address : ---  Secure to interact
