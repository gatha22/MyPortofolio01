import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

const items = [
  {
    title: "Design Hoodie Streetwear",
    description: "Desain hoodie dengan nuansa streetwear yang bold dan modern.",
    image: "/images/hoodie1.jpg"
  },
  {
    title: "Crewneck Retro Vibes",
    description: "Gaya retro dengan palet warna pastel yang cocok untuk fashion 90an.",
    image: "/images/crewneck1.jpg"
  },
  {
    title: "T-shirt Minimalist",
    description: "Kaos dengan desain minimalis, cocok untuk daily wear.",
    image: "/images/tshirt1.jpg"
  }
];

export default function Portfolio() {
  return (
    <div className="p-6 max-w-7xl mx-auto">
      <h1 className="text-4xl font-bold mb-6 text-center">Portofolio Desain Baju</h1>
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        {items.map((item, index) => (
          <motion.div
            key={index}
            whileHover={{ scale: 1.05 }}
            className="rounded-2xl shadow-lg overflow-hidden"
          >
            <Card>
              <img src={item.image} alt={item.title} className="w-full h-60 object-cover" />
              <CardContent className="p-4">
                <h2 className="text-xl font-semibold mb-2">{item.title}</h2>
                <p className="text-sm text-gray-600 mb-4">{item.description}</p>
                <Button className="w-full">Lihat Detail</Button>
              </CardContent>
            </Card>
          </motion.div>
        ))}
      </div>
    </div>
  );
}
