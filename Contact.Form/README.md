#Contact Form, for Umbraco v6.2.4 (Assembly version: 1.0.5394.15649) and up

Formul�rio de Contato para Umbraco v6.2.4 (Assembly version: 1.0.5394.15649) e acima
Criado especificamente para GSK
http://www.gsk.com/

Para d�vidas, contate carlos.casalicchio@gmail.com

Use o formul�rio inserindo um novo macro em seu html
<umbraco:Macro show_cpf="0|1" show_permit="0|1" Alias="ContactForm" runat="server"></umbraco:Macro>

Insira o css e ajuste os dados do email em App_Code/Contact_Form.cs

	public Mailer()
        {
            //Definir valores padr�o
            //Assunto
            subject = "Email recebido";
            //Corpo do email
            body="<h3>Email Recebido</h3><p><h3>Nome</h3>{0}<h3>E-mail</h3>{1}<h3>Fone</h3>{2}<h3>Cidade</h3>{3}<h3>Estado</h3>{4}<h3>Assunto</h3>{5}<h3>Categoria</h3>{6}<h3>Mensagem</h3>{7}<h3>CPF</h3>{8}<h3>N�mero do conselho</h3>{9}<h3>Tipo de Cliente</h3>{10}</p>";
            //Remetente
            from="postmaster@email.com";
            from_name="Mailer do Site";
            //Destinat�rio
            to="webmaster@email.com";
            to_name="Webmaster do Site";
            //Dados do Servidor
            smtp_usr="username"; //usu�rio smtp
            smtp_pwd="passowrd"; //senha smtp
            smtp_host="localhost"; //servidor smtp
            port=3535; //porta de envio
        }

