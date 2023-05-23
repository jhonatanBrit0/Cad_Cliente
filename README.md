# Cad_Cliente
Cadastro de Clientes Usando Framework Adianti

 // create the form fields
        $id = new THidden('id');
        
        $nome = new TEntry('nome');
        $nome->addValidation('<b>NOME</b>',new TRequiredValidator);
        $nome->forceUpperCase();
                
        $cpf = new TEntry('cpf');
        $cpf->setMask('999.999.999-99');
        $cpf->addValidation('<b>CPF</b>',new TCPFValidator);    //verifica se o cpf digitado é válido
        
        $dataNascimento = new TDate('dataNascimento');
        $dataNascimento->setMask('dd/mm/yyyy');                                      //colocanda a data na visualização padrãp para o usuario
        $dataNascimento->setDatabaseMask('yyyy-mm-dd');                              //colocando a mascara modelo/padrão americano pra salvar no BD
        $dataNascimento->addValidation('<b>DATA NASC.</b>',new TRequiredValidator);
        
        
        $telefone1 = new TEntry('telefone1');
        $telefone1->setMask('(99)99999-9999');  //definindo o modelo de digitação do telefone
        $telefone1->addValidation('<b>TELEFONE 1</b>', new TRequiredValidator);
        
        
        $telefone2 = new TEntry('telefone2');
        $telefone2->setMask('(99)99999-9999');
        
        $email = new TEntry('email');
        $email->addValidation('<b>E-Mail</b>',new TRequiredValidator);
        
        $endereco = new TEntry('endereco');
        $endereco->forceUpperCase();
        $endereco->addValidation('<b>ENDEREÇO</b>', new TRequiredValidator);
        
        $bairro = new TEntry('bairro');
        $bairro->forceUpperCase();
        $bairro->addValidation('<b>BAIRRO</b>', new TRequiredValidator);
        
        $referencia = new TEntry('referencia');
        $observacao = new TEntry('observacao');
       

