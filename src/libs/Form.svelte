<script>
    const submit = e => {
        e.preventDefault();
        const form = e.target;
        let [nome, email, telefone, texto] = [form.nome.value, form.email.value, form.telefone.value, form.texto.value];
        let query = encodeURI("Contato com a empresa\nNome:"+nome+", E-mail: "+email+", Mensagem:"+texto);
        window.open("https://api.whatsapp.com/send/?phone=5511930100006&text="+query+"&app_absent=0")
    }
</script>

<div class="mx-5 md:mx-44 min-h-screen flex flex-col justify-center items-center">
    <h1 class="font-['Cinzel'] text-3xl md:text-5xl pt-5 text-center md:px-12 mb-5">Vamos Conversar?</h1>
    <div class="relative w-32 h-1 border-b mb-4"></div>
    <div class="flex lg:flex-row flex-col w-full items-center">
        <form on:submit={submit} class="w-full lg:w-1/2 mt-10 text-center flex-[3]">
            <input name="nome" type="text" class="py-2 px-3 w-full rounded outline-none text-gray-800" placeholder="Nome Completo">
            <div class="flex space-x-2 my-2">
                <input name="email" type="email" class="py-2 px-3 w-full rounded outline-none text-gray-800" placeholder="E-mail">
                <input name="telefone" type="text"  class="py-2 px-3 w-full rounded outline-none text-gray-800" placeholder="Telefone">
            </div>
            <textarea name="texto" placeholder="Informe sua mensagem..." class="py-2 px-3 w-full h-24 rounded outline-none text-gray-800">Informe sua mensagem...</textarea>
            <button class="bg-white text-gray-800 py-3 font-bold px-12 mt-5 uppercase font-[Poppins] font-bold shadow-lg rounded">
                Enviar
            </button>
        </form>
        <div class="flex-[2] lg:ml-12 mt-6 font-['Minion-Pro-Caption'] space-y-3 text-xl text-center lg:text-left">
            <p class="flex items-center justify-center lg:justify-start"><i class="fas fa-location-dot"></i> &nbsp; Sorocaba/SP</p>
            <p class="flex items-center justify-center lg:justify-start"><i class="fas fa-phone"></i> &nbsp; (15) 3042-1851</p>
            <p class="flex items-center justify-center lg:justify-start"><i class="fas fa-envelope"></i> &nbsp; contabilcasantos@gmail.com</p>
            <p class="font-['Minion-Pro-Caption'] md:text-lg text-lg mt-10">Redes Sociais:</p>
            <div class="my-5">
                <button
                        on:click={() => { window.open("https://api.whatsapp.com/send/?phone=5511930100006&text&app_absent=0")}}
                        class="rounded-full hover:bg-white hover:text-gray-800 duration-200 border w-12 h-12 text-xl mr-3"><i class="fab fa-whatsapp"></i></button>
                <button
                        on:click={() => { window.open("https://www.instagram.com/catarinesantoscontadora/") }}
                        class="rounded-full hover:bg-white hover:text-gray-800 duration-200 border w-12 h-12 text-xl mr-3"><i class="fab fa-instagram"></i></button>
                <button
                        on:click={() => { window.open("https://facebook.com/catarinesantoscontadora") }}
                        class="rounded-full hover:bg-white hover:text-gray-800 duration-200 border w-12 h-12 text-xl"><i class="fab fa-facebook-f"></i></button>
            </div>
        </div>
    </div>
</div>
