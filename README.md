/**
 * @license
 * SPDX-License-Identifier: Apache-2.0
 */

import React from 'react';
import { 
  GraduationCap, 
  HandMetal, 
  RotateCcw, 
  Ear, 
  Star, 
  Timer, 
  ArrowRight, 
  Quote, 
  X, 
  Check, 
  Brain, 
  ShieldCheck, 
  Handshake, 
  Gauge, 
  Volume2, 
  MessageSquare, 
  Lightbulb, 
  CircleCheck, 
  CircleX, 
  Layers, 
  Stethoscope, 
  ListOrdered, 
  CheckCheck, 
  Building2, 
  Key
} from 'lucide-react';
import { motion } from 'motion/react';

const Slide = ({ children, className = "" }: { children: React.ReactNode, className?: string }) => (
  <div className={`w-[1280px] h-[720px] bg-white rounded-xl shadow-2xl overflow-hidden relative flex flex-col p-[60px] my-8 mx-auto font-sans ${className}`}>
    {/* Background Decorations */}
    <div className="absolute -top-12 -right-12 w-48 h-48 bg-brand-orange/10 rounded-full blur-3xl pointer-events-none" />
    <div className="absolute -bottom-24 -left-24 w-72 h-72 bg-brand-blue/5 rounded-full blur-3xl pointer-events-none" />
    <div className="relative z-10 flex flex-col h-full">
      {children}
    </div>
  </div>
);

const SlideTitle = ({ children }: { children: React.ReactNode }) => (
  <h2 className="text-4xl font-display font-extrabold mb-10 text-brand-blue uppercase border-l-8 border-brand-orange pl-4">
    {children}
  </h2>
);

export default function App() {
  return (
    <div className="min-h-screen py-10">
      {/* Slide 1: Title Slide */}
      <div className="w-[1280px] h-[720px] bg-brand-blue rounded-xl shadow-2xl overflow-hidden mx-auto flex items-center justify-center relative">
        {/* Background Decorations for Title Slide */}
        <div className="absolute top-0 left-0 w-full h-full opacity-10 pointer-events-none">
          <div className="absolute top-10 left-10 w-64 h-64 bg-white rounded-full blur-3xl" />
          <div className="absolute bottom-10 right-10 w-96 h-96 bg-brand-orange rounded-full blur-3xl" />
        </div>
        
        <div className="p-[60px] flex flex-col justify-center text-white text-center items-center relative z-10">
          <motion.h1 
            initial={{ opacity: 0, y: -50 }}
            animate={{ opacity: 1, y: 0 }}
            className="text-5xl font-display font-bold leading-tight uppercase mb-8"
          >
            Kỹ năng<br />
            Tiếp nhận & xử lý vấn đề triệt để
          </motion.h1>
          <motion.p 
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ delay: 0.3 }}
            className="text-3xl text-indigo-100 mb-12"
          >
            Dành cho Nhân viên DVKH Hotline
          </motion.p>
          <div className="mt-8">
            <span className="bg-brand-orange text-white px-8 py-3 rounded-full font-bold text-lg flex items-center gap-3 w-fit mx-auto shadow-lg">
              <GraduationCap size={24} /> Learning and Development Department
            </span>
          </div>
        </div>
      </div>

      {/* Slide 2: Mục tiêu */}
      <Slide>
        <SlideTitle>Mục Tiêu Bài Học</SlideTitle>
        <div className="grid grid-cols-2 gap-12 flex-grow items-center">
          <div>
            <p className="text-2xl font-bold text-brand-blue mb-8">Giúp nhân viên DVKH nâng cao khả năng:</p>
            <ul className="space-y-8">
              <li className="text-xl">
                <strong className="text-brand-orange block text-2xl mb-1">Tiếp nhận đúng vấn đề</strong>
                <span className="italic">Lắng nghe và xác định chính xác cốt lõi thông tin.</span>
              </li>
              <li className="text-xl">
                <strong className="text-brand-orange block text-2xl mb-1">Phân loại & Xử lý hiệu quả</strong>
                <span className="italic">Áp dụng quy trình chuẩn để giải quyết triệt để.</span>
              </li>
            </ul>
            <div className="mt-10 p-5 bg-slate-50 border-l-4 border-brand-orange rounded-r-lg">
              <p className="text-xl"><strong>Đích đến:</strong> Đảm bảo chỉ số hài lòng khách hàng (CSAT/NPS) ở mức cao nhất.</p>
            </div>
          </div>
          <div className="rounded-xl overflow-hidden shadow-xl h-[400px]">
            <img 
              src="https://images.unsplash.com/photo-1552581234-26160f608093?auto=format&fit=crop&q=80&w=800" 
              alt="Target" 
              className="w-full h-full object-cover"
              referrerPolicy="no-referrer"
            />
          </div>
        </div>
      </Slide>

      {/* Slide 3: Nguyên tắc */}
      <Slide>
        <SlideTitle>Nguyên Tắc Tham Gia</SlideTitle>
        <div className="grid grid-cols-3 gap-8 flex-grow items-stretch">
          {[
            { icon: <HandMetal />, title: "Chủ động & Chia sẻ", desc: "Không có câu trả lời đúng hay sai, chỉ có cách giải quyết phù hợp trong từng tình huống." },
            { icon: <RotateCcw />, title: "Thực hành & Phản hồi", desc: "Tích cực tham gia Roleplay. Đúc kết kinh nghiệm qua từng trải nghiệm thực tế cùng đồng nghiệp." },
            { icon: <Ear />, title: "Tôn trọng & Lắng nghe", desc: "Xây dựng một môi trường học tập an toàn, cởi mở và tôn trọng mọi ý kiến đóng góp." }
          ].map((item, i) => (
            <div key={i} className="bg-slate-50 border border-slate-200 rounded-xl p-10 flex flex-col items-center text-center shadow-sm">
              <div className="w-24 h-24 bg-brand-orange/10 rounded-full flex items-center justify-center text-brand-orange mb-6">
                {item.icon}
              </div>
              <h3 className="text-2xl font-display font-bold text-brand-blue mb-4">{item.title}</h3>
              <p className="text-lg text-slate-600 leading-relaxed">{item.desc}</p>
            </div>
          ))}
        </div>
      </Slide>

      {/* Slide 4: Quy trình 5 bước */}
      <Slide>
        <SlideTitle>Quy Trình Cuộc Gọi Hotline 5 Bước</SlideTitle>
        <div className="flex-grow flex flex-col justify-center">
          <div className="relative py-10">
            <div className="absolute top-1/2 left-0 w-full h-1.5 bg-slate-200 -translate-y-1/2 rounded-full" />
            <div className="flex justify-between relative z-10">
              {[
                { step: "BƯỚC 1", title: "Chào hỏi", desc: "Tạo thiện cảm ban đầu" },
                { step: "BƯỚC 2", title: "Khai thác vấn đề & Hỗ trợ", desc: "Trọng tâm bài học", active: true },
                { step: "BƯỚC 3", title: "Xác nhận", desc: "Đảm bảo hỗ trợ xong" },
                { step: "BƯỚC 4", title: "Chào kết thúc", desc: "Để lại ấn tượng tốt" },
                { step: "BƯỚC 5", title: "Tạo ticket", desc: "Ghi nhận hệ thống" }
              ].map((item, i) => (
                <div key={i} className="w-[18%] text-center relative">
                  <div className={`w-7 h-7 rounded-full border-4 mx-auto mb-10 bg-white ${item.active ? 'border-brand-orange bg-brand-orange' : 'border-brand-blue'}`} />
                  <div className={`absolute w-full ${i % 2 === 0 ? 'bottom-full mb-8' : 'top-full mt-8'}`}>
                    <h3 className={`text-xl font-bold mb-2 ${item.active ? 'text-brand-orange' : 'text-brand-blue'}`}>{item.step}</h3>
                    <p className="text-sm font-bold">{item.title}</p>
                    <p className="text-xs text-slate-500">{item.desc}</p>
                  </div>
                </div>
              ))}
            </div>
          </div>
          <p className="text-center mt-32 font-bold text-brand-orange text-2xl flex items-center justify-center gap-2">
            <Star className="fill-brand-orange" /> Highlight: Bài học hôm nay đi sâu vào kỹ năng xử lý tại Bước 2.
          </p>
        </div>
      </Slide>

      {/* Slide 5: Quản trị cảm xúc */}
      <Slide>
        <SlideTitle>1.1 Lắng Nghe Hiệu Quả - Quản Trị Cảm Xúc</SlideTitle>
        <div className="flex flex-col flex-grow justify-center max-w-3xl mx-auto w-full">
          <p className="text-xl mb-8 text-center">Nhận diện cảm xúc của chính mình trước khi xử lý vấn đề của khách hàng.</p>
          <div className="bg-slate-50 p-8 rounded-xl border border-slate-200 shadow-sm">
            <h3 className="text-2xl font-bold text-brand-orange mb-6 flex items-center justify-center gap-2">
              <Timer /> Kỹ thuật 3-3-1
            </h3>
            <ul className="space-y-4 mb-8 max-w-md mx-auto">
              <li className="flex items-center gap-3 text-lg font-bold">
                <ArrowRight className="text-brand-blue" /> Hít sâu 3 giây
              </li>
              <li className="flex items-center gap-3 text-lg font-bold">
                <ArrowRight className="text-brand-blue" /> Thở chậm 3 giây
              </li>
              <li className="flex items-center gap-3 text-lg font-bold">
                <ArrowRight className="text-brand-blue" /> Gọi tên 1 cảm xúc xuất hiện
              </li>
            </ul>
            <div className="pt-6 border-t border-dashed border-slate-300 text-center">
              <p className="text-brand-blue font-bold text-lg leading-relaxed italic">
                Gọi tên cảm xúc = Kích hoạt tư duy logic = Ngắt phản xạ "xù lông"
              </p>
            </div>
          </div>
        </div>
      </Slide>

      {/* Slide 6: Bảng Cảm Xúc */}
      <Slide className="font-['Inter']">
        <h2 className="text-[40px] font-bold font-['Roboto'] mb-[30px] text-[#1a4f4c] text-left w-full">
          Bạn Đang Cảm Thấy Thế Nào?
        </h2>
        <div className="flex-grow flex flex-col items-center justify-center w-full">
          <div className="grid grid-cols-6 grid-rows-5 gap-3 w-full h-full max-h-[560px]">
            {[
              { text: "Hào Hứng", icon: "fa-regular fa-face-laugh-beam" },
              { text: "Hoang Mang", icon: "fa-regular fa-face-dizzy" },
              { text: "Khó Hiểu", icon: "fa-regular fa-face-flushed" },
              { text: "Biết Ơn", icon: "fa-regular fa-face-smile-beam" },
              { text: "Thoải Mái", icon: "fa-regular fa-face-smile" },
              { text: "Chán Nản", icon: "fa-regular fa-face-frown" },
              { text: "Hy Vọng", icon: "fa-regular fa-face-grin-squint" },
              { text: "Mất Tập Trung", icon: "fa-regular fa-face-meh-blank" },
              { text: "Vui Vẻ", icon: "fa-regular fa-face-laugh" },
              { text: "Nóng Lòng", icon: "fa-regular fa-face-grimace" },
              { text: "Mệt Mỏi", icon: "fa-regular fa-face-tired" },
              { text: "Chủ Động", icon: "fa-regular fa-face-grin-wink" },
              { text: "Lạc Lõng", icon: "fa-regular fa-face-frown-open" },
              { text: "Tò Mò", icon: "fa-regular fa-face-surprise" },
              { text: "Thích Thú", icon: "fa-regular fa-face-grin-stars" },
              { text: "Sung Sướng", icon: "fa-regular fa-face-laugh-squint" },
              { text: "Hối Hận", icon: "fa-regular fa-face-sad-cry" },
              { text: "Bất Ngờ", icon: "fa-solid fa-face-surprise" },
              { text: "Khó Chịu", icon: "fa-regular fa-face-angry" },
              { text: "May Mắn", icon: "fa-regular fa-face-grin" },
              { text: "Kết Nối", icon: "fa-regular fa-face-smile-wink" },
              { text: "Lo Lắng", icon: "fa-regular fa-face-sad-tear" },
              { text: "Ngại Ngùng", icon: "fa-regular fa-face-flushed" },
              { text: "Toại Nguyện", icon: "fa-regular fa-face-laugh-beam" },
              { text: "Tự Hào", icon: "fa-regular fa-face-grin-squint-tears" },
              { text: "Nhẹ Nhõm", icon: "fa-regular fa-face-smile" },
              { text: "Có Lỗi", icon: "fa-regular fa-face-sad-tear" },
              { text: "Tự Ti", icon: "fa-regular fa-face-frown" },
              { text: "Bình Yên", icon: "fa-regular fa-face-meh" },
              { text: "Kính Phục", icon: "fa-regular fa-face-grin-stars" },
            ].map((emotion, idx) => (
              <div key={idx} className="bg-white rounded-md border-[2.5px] border-[#5faea9] flex flex-col items-center justify-center p-2.5 text-center transition-transform hover:scale-105">
                <span className="text-[#1e3f3d] font-['Roboto'] text-[15px] font-bold tracking-wider mb-3 uppercase leading-[1.1]">
                  {emotion.text}
                </span>
                <i className={`${emotion.icon} text-[#5faea9] text-[38px] font-light`}></i>
              </div>
            ))}
          </div>
        </div>
      </Slide>



      {/* Slide 7: Tư duy dịch vụ */}
      <Slide>
        <SlideTitle>Tư Duy Dịch Vụ - 3 Kỳ Vọng Của Khách Hàng</SlideTitle>
        <div className="grid grid-cols-3 gap-8 flex-grow">
          {[
            { icon: <Brain />, title: "Có người HIỂU vấn đề", desc: "Khách hàng muốn trình bày và được lắng nghe trọn vẹn, không bị ngắt lời hay phán xét sai/đúng ngay từ đầu." },
            { icon: <ShieldCheck />, title: "Có người CHỊU TRÁCH NHIỆM", desc: "Khách hàng cần một đại diện từ công ty nhận lỗi hoặc ghi nhận sự cố thay vì đùn đẩy trách nhiệm." },
            { icon: <Handshake />, title: "Có người XỬ LÝ CÙNG", desc: "Khách hàng mong muốn một giải pháp cụ thể và sự đồng hành cho đến khi sự việc được giải quyết triệt để." }
          ].map((item, i) => (
            <div key={i} className="bg-slate-50 border border-slate-200 rounded-xl p-8 flex flex-col items-center text-center">
              <div className="w-20 h-20 bg-brand-orange/10 rounded-full flex items-center justify-center text-brand-orange mb-6">
                {item.icon}
              </div>
              <h3 className="text-xl font-bold text-brand-blue mb-4 leading-tight">
                {item.title.split(' ').map((word, idx) => word === 'HIỂU' || word === 'CHỊU' || word === 'TRÁCH' || word === 'NHIỆM' || word === 'XỬ' || word === 'LÝ' || word === 'CÙNG' ? <span key={idx} className="text-brand-orange">{word} </span> : word + ' ')}
              </h3>
              <p className="text-slate-600">{item.desc}</p>
            </div>
          ))}
        </div>
        <div className="mt-10 bg-brand-blue p-6 rounded-xl text-center">
          <p className="text-white text-3xl font-display font-bold flex items-center justify-center gap-4">
            <Quote className="text-brand-orange rotate-180" /> THẤU HIỂU TRƯỚC - GIẢI THÍCH SAU <Quote className="text-brand-orange" />
          </p>
        </div>
      </Slide>

      {/* Slide 8: Giọng nói */}
      <Slide>
        <SlideTitle>Điều Chỉnh Giọng Nói - "Xoa Dịu" Cảm Xúc</SlideTitle>
        <div className="grid grid-cols-2 gap-10 flex-grow">
          <div className="bg-slate-50 rounded-xl p-10 border border-slate-200">
            <h3 className="text-2xl font-bold text-brand-blue mb-8">3 Yếu Tố Tác Động</h3>
            <ul className="space-y-8">
              <li className="border-b border-slate-200 pb-6">
                <strong className="text-brand-blue text-xl flex items-center gap-2 mb-2">
                  <Gauge className="text-brand-orange" /> Tốc độ:
                </strong>
                <p className="italic">Vừa phải, rõ ràng<br />(Tuyệt đối không cuốn theo nhịp điệu gấp gáp của khách).</p>
              </li>
              <li className="border-b border-slate-200 pb-6">
                <strong className="text-brand-blue text-xl flex items-center gap-2 mb-2">
                  <Volume2 className="text-brand-orange" /> Âm lượng:
                </strong>
                <p className="italic">Ổn định, trầm ấm<br />(Không nâng tone giọng dù khách hàng có lớn tiếng).</p>
              </li>
              <li>
                <strong className="text-brand-blue text-xl flex items-center gap-2 mb-2">
                  <MessageSquare className="text-brand-orange" /> Ngôn từ:
                </strong>
                <p className="italic">Tích cực, hướng tới giải pháp.</p>
              </li>
            </ul>
          </div>
          <div className="bg-orange-50 rounded-xl p-10 border border-orange-200">
            <h3 className="text-2xl font-bold text-orange-800 mb-8 flex items-center gap-2">
              <Lightbulb /> Tip Box
            </h3>
            <div className="space-y-8">
              <div>
                <p className="font-bold text-green-700 text-xl mb-4 flex items-center gap-2">
                  <CircleCheck size={20} /> Nên dùng:
                </p>
                <ul className="list-disc pl-8 italic text-slate-700 space-y-2">
                  <li>"Để em kiểm tra chi tiết cho anh/chị..."</li>
                  <li>"Dạ, em hiểu sự bất tiện này rồi ạ."</li>
                  <li>"Em sẽ hỗ trợ mình xử lý bước này..."</li>
                </ul>
              </div>
              <div>
                <p className="font-bold text-red-700 text-xl mb-4 flex items-center gap-2">
                  <CircleX size={20} /> Tránh dùng:
                </p>
                <ul className="list-disc pl-8 italic text-slate-700 space-y-2">
                  <li>"Em đã nói với anh rồi mà..."</li>
                  <li>"Cái này do anh thao tác sai rồi."</li>
                  <li>"Bên em không có lỗi trong chuyện này."</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </Slide>

      {/* Slide 9: 3 Tầng thông tin */}
      <Slide>
        <SlideTitle>1.2 Xác Nhận Đúng Vấn Đề - 3 Tầng Thông Tin</SlideTitle>
        <div className="grid grid-cols-2 gap-12 flex-grow items-center">
          <div className="space-y-6">
            <div className="bg-slate-50 p-6 rounded-lg border-l-4 border-brand-blue">
              <strong className="text-brand-blue text-xl block mb-1">Tầng 1: Sự việc</strong>
              <p>Điều gì đang thực sự xảy ra với khách hàng?</p>
            </div>
            <div className="bg-blue-50 p-6 rounded-lg border-l-4 border-blue-500">
              <strong className="text-brand-blue text-xl block mb-1">Tầng 2: Tác động</strong>
              <p>Sự việc này ảnh hưởng thế nào đến công việc/trải nghiệm của họ?</p>
            </div>
            <div className="bg-red-50 p-6 rounded-lg border-l-4 border-red-500">
              <strong className="text-brand-orange text-xl block mb-1">Tầng 3: Mối lo ngại (Quan trọng nhất)</strong>
              <p>Điều gì khiến khách hàng cảm thấy lo sợ nhất đằng sau sự việc?</p>
            </div>
            <p className="font-bold text-green-800 text-center pt-4">
              <Key className="inline text-brand-orange mr-2" /> Giải quyết được "Mối lo ngại" = Khách hàng hài lòng.
            </p>
          </div>
          <div className="h-[500px] flex items-center justify-center">
            <img 
              src="https://pitel.vn/wp-content/uploads/2025/01/1-Khong-chi-tra-loi-cau-hoi-tong-dai-vien-con-la-cau-noi-giua-thuong-hieu-va-khach-hang.png" 
              alt="Call Center Bridge" 
              className="rounded-xl shadow-2xl h-full object-cover"
              referrerPolicy="no-referrer"
            />
          </div>
        </div>
      </Slide>

      {/* Slide 10: Tips lắng nghe */}
      <Slide>
        <SlideTitle>Tips Lắng Nghe Chủ Động</SlideTitle>
        <div className="grid grid-cols-3 gap-8 flex-grow">
          {[
            { icon: <Timer />, title: "Quy tắc 60-90s", desc: "Tuyệt đối không ngắt lời khách hàng trong 1 phút rưỡi đầu tiên. Đây là \"thời gian vàng\" để họ xả cảm xúc và trình bày sự việc." },
            { icon: <MessageSquare />, title: "Từ khóa tương tác", desc: "Thể hiện bạn vẫn đang tập trung bằng các câu đệm ngắn gọn:\n\n\"Dạ em đang nghe\"\n\"Vâng, em vẫn đang ghi nhận ạ\"" },
            { icon: <Handshake />, title: "Kỹ thuật ghi chú", desc: "Không chép chính tả. Hãy gạch đầu dòng bằng các Từ khóa tương ứng với 3 tầng thông tin: Sự việc - Tác động - Mối lo ngại." }
          ].map((item, i) => (
            <div key={i} className="bg-slate-50 border border-slate-200 rounded-xl p-10 flex flex-col items-center text-center shadow-sm">
              <div className="w-20 h-20 bg-brand-orange/10 rounded-full flex items-center justify-center text-brand-orange mb-6">
                {item.icon}
              </div>
              <h3 className="text-2xl font-bold text-brand-blue mb-6">{item.title}</h3>
              <p className="text-slate-600 whitespace-pre-line">{item.desc}</p>
            </div>
          ))}
        </div>
      </Slide>

      {/* Slide 11a: Cấu trúc xác nhận - Công thức */}
      <Slide>
        <SlideTitle>Cấu Trúc Xác Nhận Hiệu Quả - Công Thức Chuẩn</SlideTitle>
        <div className="flex-grow flex flex-col justify-center max-w-4xl mx-auto w-full">
          <div className="bg-brand-blue p-10 rounded-2xl text-center mb-12 shadow-xl">
            <p className="text-white font-bold text-4xl">
              Xác nhận = <span className="text-brand-orange">[Vấn đề]</span> + <span className="text-brand-orange">[Tác động]</span> + <span className="text-brand-orange">[Mối lo ngại]</span>
            </p>
          </div>
          <div className="space-y-6">
            <h4 className="text-brand-orange text-2xl font-bold flex items-center gap-2">
              <Lightbulb /> Ví dụ mẫu:
            </h4>
            <div className="bg-slate-50 p-10 rounded-xl border border-slate-200 shadow-inner">
              <p className="text-2xl italic leading-relaxed text-slate-700">
                "Dạ <strong>chị Trang</strong>, em xác nhận lại là <strong>bill báo bếp không in được</strong> (Vấn đề), khiến việc <strong>phục vụ đang lộn xộn</strong> (Tác động), và chị đang rất lo <strong>khách phàn nàn bỏ về</strong> đúng không ạ?" (Mối lo ngại)
              </p>
            </div>
          </div>
        </div>
      </Slide>

      {/* Slide 11b: Cấu trúc xác nhận - Lưu ý */}
      <Slide>
        <SlideTitle>Cấu Trúc Xác Nhận Hiệu Quả - Lưu Ý Quan Trọng</SlideTitle>
        <div className="grid grid-cols-2 gap-12 flex-grow items-center">
          <div className="bg-slate-50 p-10 rounded-xl border border-slate-200 h-full">
            <h3 className="text-2xl font-bold text-brand-blue mb-8">Nguyên tắc 3 KHÔNG:</h3>
            <ul className="space-y-8">
              <li className="flex gap-4">
                <div className="w-8 h-8 bg-red-100 text-red-600 rounded-full flex items-center justify-center shrink-0 font-bold">1</div>
                <div>
                  <strong className="text-xl block mb-1">Không lặp y nguyên</strong>
                  <p>Khách nói 10 câu, hãy tóm gọn lại 2 câu cốt lõi.</p>
                </div>
              </li>
              <li className="flex gap-4">
                <div className="w-8 h-8 bg-red-100 text-red-600 rounded-full flex items-center justify-center shrink-0 font-bold">2</div>
                <div>
                  <strong className="text-xl block mb-1">Không suy diễn</strong>
                  <p>Chỉ xác nhận những gì khách đã chia sẻ.</p>
                </div>
              </li>
              <li className="flex gap-4">
                <div className="w-8 h-8 bg-red-100 text-red-600 rounded-full flex items-center justify-center shrink-0 font-bold">3</div>
                <div>
                  <strong className="text-xl block mb-1">Không vội giải thích</strong>
                  <p>Khoan nói "tại sao lỗi", hãy cho khách biết "mình đã hiểu lỗi".</p>
                </div>
              </li>
            </ul>
          </div>
          <div className="bg-blue-50 p-10 rounded-xl border border-blue-200 h-full flex flex-col justify-center">
            <div className="mb-8">
              <p className="text-xl font-bold text-brand-blue mb-4 flex items-center gap-2">
                <Lightbulb className="text-brand-orange" /> Mẹo ngắt lời lịch sự:
              </p>
              <p className="text-xl italic text-slate-700 bg-white p-6 rounded-lg border border-blue-100">
                "Dạ, cho em xin phép tóm tắt lại một chút để đảm bảo em hỗ trợ mình chính xác nhất nhé..."
              </p>
            </div>
            <p className="text-slate-500 text-sm italic">* Sử dụng khi khách hàng trình bày quá dài hoặc lan man.</p>
          </div>
        </div>
      </Slide>

      {/* Slide 12: Nhóm vấn đề */}
      <Slide>
        <SlideTitle>2.1 Bốn Nhóm Vấn Đề Thường Gặp</SlideTitle>
        <div className="flex-grow">
          <table className="w-full border-collapse rounded-xl overflow-hidden shadow-lg">
            <thead>
              <tr className="bg-brand-blue text-white text-left">
                <th className="p-6 text-xl font-display font-bold w-1/4"><Layers className="inline mr-2" /> Nhóm Vấn Đề</th>
                <th className="p-6 text-xl font-display font-bold"><Stethoscope className="inline mr-2" /> Bảng Chẩn Đoán Nhanh & Dấu Hiệu</th>
              </tr>
            </thead>
            <tbody className="text-lg">
              <tr className="bg-white border-b border-slate-100">
                <td className="p-6 font-bold">1. Lỗi kỹ thuật</td>
                <td className="p-6">Hệ thống không phản hồi, phần mềm bị văng (crash), lỗi kết nối mạng, thiết bị phần cứng không hoạt động.</td>
              </tr>
              <tr className="bg-slate-50 border-b border-slate-100">
                <td className="p-6 font-bold">2. Hướng dẫn sử dụng</td>
                <td className="p-6">Khách hàng chưa biết cách thao tác một tính năng mới, quên mật khẩu, không tìm thấy nút chức năng.</td>
              </tr>
              <tr className="bg-white border-b border-slate-100">
                <td className="p-6 font-bold">3. Khiếu nại</td>
                <td className="p-6">Phàn nàn về thái độ nhân viên, không hài lòng với chính sách công ty, chất lượng dịch vụ không như cam kết.</td>
              </tr>
              <tr className="bg-slate-50">
                <td className="p-6 font-bold">4. Yêu cầu hỗ trợ</td>
                <td className="p-6">Cần thay đổi thông tin hợp đồng, thêm phân quyền tài khoản mới, yêu cầu setup lại hệ thống chi nhánh.</td>
              </tr>
            </tbody>
          </table>
        </div>
      </Slide>

      {/* Slide 13: Kỹ năng xử lý */}
      <Slide>
        <SlideTitle>2.2 Kỹ Năng Xử Lý Vấn Đề Hiệu Quả</SlideTitle>
        <div className="grid grid-cols-2 gap-12 flex-grow items-center">
          <div>
            <p className="text-2xl font-bold text-brand-blue mb-8">Nguyên Tắc Truyền Đạt Hướng Dẫn</p>
            <div className="space-y-6">
              {[
                { icon: <MessageSquare />, title: "Nói ngôn ngữ của khách hàng", desc: "Chuyển đổi các thuật ngữ chuyên môn IT phức tạp thành từ ngữ thông dụng, dễ hiểu." },
                { icon: <ListOrdered />, title: "Chia nhỏ quy trình", desc: "Đừng đưa một lúc 5 bước. Hãy hướng dẫn: Bước 1 -> Bước 2." },
                { icon: <CheckCheck />, title: "Xác nhận từng nấc", desc: "Chỉ khi khách hàng xác nhận đã làm được bước A, mới tiếp tục hướng dẫn sang bước B." }
              ].map((item, i) => (
                <div key={i} className="bg-slate-50 p-6 rounded-xl border border-slate-200 flex gap-6">
                  <div className="text-brand-orange shrink-0">{item.icon}</div>
                  <div>
                    <strong className="text-xl block mb-1 text-brand-blue">{item.title}</strong>
                    <p className="text-slate-600">{item.desc}</p>
                  </div>
                </div>
              ))}
            </div>
          </div>
          <div className="h-[450px] rounded-xl overflow-hidden shadow-2xl">
            <img 
              src="https://images.unsplash.com/photo-1507208773393-40d9fc670acf?auto=format&fit=crop&q=80&w=800" 
              alt="Step by step" 
              className="w-full h-full object-cover"
              referrerPolicy="no-referrer"
            />
          </div>
        </div>
      </Slide>

      {/* Slide 14: Checklist */}
      <Slide>
        <SlideTitle>Checklist Tiếp Nhận & Xử Lý</SlideTitle>
        <div className="grid grid-cols-2 gap-8 flex-grow">
          {[
            { title: "1. Kiểm Soát Cảm Xúc", desc: "Giữ vững kỹ thuật 3-3-1, duy trì giọng điệu âm lượng ổn định và ngôn từ tích cực." },
            { title: "2. Lắng Nghe Đủ 3 Tầng", desc: "Áp dụng quy tắc 60-90s, tìm ra Sự việc, Tác động và Mối lo ngại cốt lõi." },
            { title: "3. Xác Nhận Trước Khi Làm", desc: "Sử dụng công thức tóm tắt ngắn gọn, đảm bảo cả 2 bên đang hiểu chung 1 vấn đề." },
            { title: "4. Chẩn Đoán & Trình Bày", desc: "Phân loại đúng nhóm lỗi, chia nhỏ quy trình và hướng dẫn bằng ngôn ngữ đơn giản." }
          ].map((item, i) => (
            <div key={i} className="bg-slate-50 p-8 rounded-xl border border-slate-200 flex gap-6 items-start shadow-sm">
              <CircleCheck className="text-brand-orange shrink-0" size={40} />
              <div>
                <strong className="text-2xl block mb-2 text-brand-blue">{item.title}</strong>
                <p className="text-lg text-slate-600">{item.desc}</p>
              </div>
            </div>
          ))}
        </div>
      </Slide>

      {/* Slide 15: Roleplay */}
      <Slide>
        <SlideTitle>Roleplay - Tình Huống Thực Tế</SlideTitle>
        <div className="flex-grow flex flex-col justify-center">
          <div className="bg-slate-50 p-12 rounded-2xl border border-slate-200 shadow-lg relative">
            <div className="absolute -top-6 left-12 bg-brand-orange text-white px-6 py-2 rounded-full font-bold flex items-center gap-2">
              <Building2 size={20} /> Bối cảnh: Quản lý nhà hàng giờ cao điểm - App xoay mòng mòng - Không in được bill.
            </div>
            <blockquote className="text-2xl italic leading-relaxed text-slate-700 relative">
              <Quote className="absolute -top-6 -left-8 text-brand-orange/20 w-16 h-16 rotate-180" />
              "Alo tổng đài phải không? Em ơi kiểm tra ngay cho anh cái phần mềm, làm ăn chán quá! Đang giờ cao điểm khách đông nghẹt mà app trên máy tính bảng cứ xoay mòng mòng, bấm thanh toán không được. Rồi bill báo bếp cũng không in ra luôn! Giờ nhân viên của anh cứ phải chạy lên chạy xuống hét order vào bếp, mệt đứt cả hơi mà đồ ăn thì lên sai bét nhè. Khách người ta đang chửi ầm lên kia kìa. Cứ cái kiểu này là mất hết khách, thất thoát doanh thu ai đền cho anh? Bên em giải quyết ngay đi, nhanh lên!"
              <Quote className="absolute -bottom-6 -right-8 text-brand-orange/20 w-16 h-16" />
            </blockquote>
            <div className="mt-10 pt-6 border-t border-slate-200 text-center">
              <p className="text-slate-500 font-bold uppercase tracking-widest">Lời thoại mở đầu (Trút giận liên tục trong 1 phút)</p>
            </div>
          </div>
        </div>
      </Slide>

      {/* Slide 16: Đúc kết */}
      <Slide>
        <SlideTitle>Đúc Kết Cá Nhân (Mô Hình 3-2-1)</SlideTitle>
        <div className="grid grid-cols-3 gap-8 flex-grow">
          {[
            { num: "3", color: "text-brand-orange", label: "Điều Quan Trọng Nhất", desc: "Đã học được từ buổi đào tạo hôm nay về kỹ năng lắng nghe và thấu hiểu." },
            { num: "2", color: "text-brand-blue", label: "Lỗi Thường Mắc Phải", desc: "Bản thân hay gặp khi tiếp nhận và xử lý sự cố cho khách hàng qua điện thoại." },
            { num: "1", color: "text-green-700", label: "Hành Động Thay Đổi", desc: "Cam kết thực hiện ngay vào ca làm việc ngày mai để cải thiện chất lượng cuộc gọi." }
          ].map((item, i) => (
            <div key={i} className="bg-slate-50 border border-slate-200 rounded-xl p-10 flex flex-col items-center text-center shadow-sm">
              <div className={`text-9xl font-display font-bold leading-none mb-6 ${item.color}`}>{item.num}</div>
              <h3 className="text-xl font-bold text-brand-blue mb-4">{item.label}</h3>
              <p className="text-slate-600">{item.desc}</p>
            </div>
          ))}
        </div>
      </Slide>

      {/* Slide 17: Thông điệp cuối */}
      <div className="w-[1280px] h-[720px] rounded-xl shadow-2xl overflow-hidden mx-auto relative flex items-center justify-center">
        <img 
          src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&q=80&w=1200" 
          alt="Teamwork" 
          className="absolute inset-0 w-full h-full object-cover"
          referrerPolicy="no-referrer"
        />
        <div className="absolute inset-0 bg-brand-blue/85 backdrop-blur-[2px]" />
        <div className="relative z-10 text-center max-w-4xl p-12">
          <motion.h2 
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            className="text-6xl font-display font-bold text-white mb-12 uppercase"
          >
            Ghi nhớ
          </motion.h2>
          <div className="text-left inline-block mb-12">
            <p className="font-bold text-brand-orange text-2xl mb-6 text-center">4 Hành Động Cốt Lõi:</p>
            <ul className="grid grid-cols-2 gap-x-12 gap-y-4">
              {[
                "Kiểm soát cảm xúc",
                "Xác nhận 3 tầng thông tin",
                "Phân loại đúng",
                "Trình bày mạch lạc"
              ].map((item, i) => (
                <li key={i} className="text-indigo-100 text-2xl flex items-center gap-4">
                  <Check className="text-brand-orange" size={28} /> {item}
                </li>
              ))}
            </ul>
          </div>
          <div className="pt-10 border-t border-white/20">
            <p className="text-4xl font-display font-bold text-white italic">
              "Chúc các bạn tự tin chinh phục mọi cuộc gọi!"
            </p>
          </div>
        </div>
      </div>
    </div>
  );
}

