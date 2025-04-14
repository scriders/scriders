import { useState } from "react";
import { Button } from "@/components/ui/button";

export default function HomePage() {
  const [email, setEmail] = useState("");

  return (
    <div className="bg-black text-white min-h-screen font-sans">
      <header className="flex justify-between items-center p-6 border-b border-white">
        <img src="/logo.png" alt="SC Riders" className="h-12" />
        <nav className="space-x-4">
          <a href="#loja" className="hover:text-sand">Loja</a>
          <a href="#manifesto" className="hover:text-sand">Manifesto</a>
          <a href="#comunidade" className="hover:text-sand">Comunidade</a>
          <a href="#portfolio" className="hover:text-sand">Portfólio</a>
          <a href="#blog" className="hover:text-sand">Blog</a>
        </nav>
      </header>

      <main className="p-6">
        <section className="relative h-[90vh] flex flex-col items-center justify-center text-center bg-cover bg-center" style={{ backgroundImage: "url('/hero.jpg')" }}>
          <div className="bg-black bg-opacity-60 p-6 rounded-xl">
            <h1 className="text-4xl md:text-6xl font-bold">Liberdade não se explica. Se vive.</h1>
            <p className="mt-4 text-xl text-gray-300">Vista sua jornada. Sinta a estrada com a SC Riders.</p>
            <Button className="mt-6 bg-white text-black hover:bg-sand">Conheça a coleção</Button>
          </div>
        </section>

        <section id="manifesto" className="py-16 border-t border-white bg-gray-900">
          <h2 className="text-3xl font-bold text-center">Manifesto</h2>
          <p className="max-w-3xl mx-auto text-center text-gray-300 text-lg mt-6">Somos mais que uma marca. Somos o ronco na estrada, o cheiro de poeira, a chuva no visor e o nascer do sol na serra. Cada peça da SC Riders carrega o espírito de quem escolhe a liberdade como estilo de vida. Aqui, cada curva é uma história, cada quilômetro, um manifesto de quem não abre mão de viver intensamente.</p>
        </section>

        <section id="loja" className="py-16 border-t border-white">
          <h2 className="text-3xl font-bold text-center">Loja</h2>
          <p className="text-center text-gray-300 mb-8">Produtos com estilo e proteção para todos os tipos de viagem.</p>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
            <div className="bg-white text-black p-4 rounded-xl">Jaqueta Touring</div>
            <div className="bg-white text-black p-4 rounded-xl">Camiseta SC Riders</div>
            <div className="bg-white text-black p-4 rounded-xl">Luvas Adventure</div>
          </div>
        </section>

        <section id="comunidade" className="py-16 border-t border-white bg-gray-900">
          <h2 className="text-3xl font-bold text-center">Comunidade SC Riders</h2>
          <p className="text-center text-gray-400 mb-8">Conecte-se com outros pilotos, compartilhe rotas e aventuras.</p>
          <Button className="block mx-auto bg-white text-black hover:bg-sand">Junte-se a nós</Button>
        </section>

        <section id="portfolio" className="py-16 border-t border-white">
          <h2 className="text-3xl font-bold text-center">Portfólio</h2>
          <p className="text-center text-gray-300 mb-8">Nossas peças, nosso estilo, sua estrada.</p>
          <div className="grid grid-cols-2 md:grid-cols-4 gap-4">
            <div className="bg-gray-800 h-32 rounded-xl"></div>
            <div className="bg-gray-800 h-32 rounded-xl"></div>
            <div className="bg-gray-800 h-32 rounded-xl"></div>
            <div className="bg-gray-800 h-32 rounded-xl"></div>
          </div>
        </section>

        <section id="blog" className="py-16 border-t border-white bg-gray-900">
          <h2 className="text-3xl font-bold text-center">Blog</h2>
          <p className="text-center text-gray-400 mb-8">Histórias da estrada, fotos da galera e dicas para rodar melhor.</p>
          <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div className="bg-white text-black p-4 rounded-xl">Post do Blog 1</div>
            <div className="bg-white text-black p-4 rounded-xl">Post do Blog 2</div>
          </div>
        </section>

        <section id="newsletter" className="py-16 border-t border-white text-center">
          <h2 className="text-3xl font-bold">Entre na estrada com a gente</h2>
          <p className="text-gray-300 mb-4">Receba novidades, cupons e histórias direto no seu e-mail.</p>
          <input
            type="email"
            value={email}
            onChange={(e) => setEmail(e.target.value)}
            placeholder="Digite seu e-mail"
            className="p-2 rounded-lg text-black mr-2"
          />
          <Button className="bg-white text-black hover:bg-sand">Inscrever</Button>
        </section>
      </main>

      <footer className="text-center p-6 border-t border-white text-gray-500 text-sm">
        © {new Date().getFullYear()} SC Riders. Todos os direitos reservados.
      </footer>
    </div>
  );
}
