---
title: Получение сведений об упаковщиках и декомпрессорах
description: Получение сведений об упаковщиках и декомпрессорах
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Диспетчер сжатия видео (ВКМ), получение сведений об компрессорах
- ВКМ (диспетчер сжатия видео), получение сведений об компрессорах
- Функция Икжетинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986521"
---
# <a name="getting-information-about-compressors-and-decompressors"></a><span data-ttu-id="972e3-106">Получение сведений об упаковщиках и декомпрессорах</span><span class="sxs-lookup"><span data-stu-id="972e3-106">Getting Information About Compressors and Decompressors</span></span>

<span data-ttu-id="972e3-107">Чтобы получить общие сведения об упаковщике или декомпрессоре, приложение может использовать функцию [**икжетинфо**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) .</span><span class="sxs-lookup"><span data-stu-id="972e3-107">To get general information about a compressor or decompressor, your application can use the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function.</span></span> <span data-ttu-id="972e3-108">Эта функция заполняет структуру [**иЦинфо**](/windows/desktop/api/Vfw/ns-vfw-icinfo) информацией об компрессоре или декомпрессоре.</span><span class="sxs-lookup"><span data-stu-id="972e3-108">This function fills an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure with information about the compressor or decompressor.</span></span> <span data-ttu-id="972e3-109">Приложение должно выделить память для структуры **иЦинфо** и передать в **икжетинфо** указатель на него.</span><span class="sxs-lookup"><span data-stu-id="972e3-109">Your application must allocate the memory for the **ICINFO** structure and pass a pointer to it in **ICGetInfo**.</span></span> <span data-ttu-id="972e3-110">Если приложение не выполняет поиск определенного средства сжатия или распаковки, флаги в структуре **иЦинфо** предоставляют наиболее полезную информацию о возможностях сжатия или распаковки.</span><span class="sxs-lookup"><span data-stu-id="972e3-110">Unless your application searches for a particular compressor or decompressor, the flags in the **ICINFO** structure provide the most useful information about the capabilities of a compressor or decompressor.</span></span>

<span data-ttu-id="972e3-111">Чтобы получить по умолчанию частоту ключей и качества кадров по умолчанию для сжатия или декомпрессора, приложение может отправить [**сообщения \_ ICM Жетдефаулткэйфрамерате**](icm-getdefaultkeyframerate.md) и [**ICM \_ жетдефаулткуалити**](icm-getdefaultquality.md) (или использовать макросы [**икжетдефаулткэйфрамерате**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) и [**икжетдефаулткуалити**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).</span><span class="sxs-lookup"><span data-stu-id="972e3-111">To get the default key-frame rate and default quality value of a compressor or decompressor, your application can send the [**ICM\_GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) and [**ICM\_GETDEFAULTQUALITY**](icm-getdefaultquality.md) messages (or use the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros).</span></span>

<span data-ttu-id="972e3-112">Чтобы определить оптимальный формат изображения для сжатия или распаковки, приложение может использовать функцию [**икжетдисплайформат**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .</span><span class="sxs-lookup"><span data-stu-id="972e3-112">To determine the best display format of a compressor or decompressor, your application can use the [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) function.</span></span>

<span data-ttu-id="972e3-113">Чтобы определить, может ли программа сжатия или декомпрессора отображать диалоговое окно о программе, отправьте сообщение [**ICM \_ о**](icm-about.md) сообщении (или используйте макрос [**иккуерябаут**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ).</span><span class="sxs-lookup"><span data-stu-id="972e3-113">To determine if a compressor or decompressor can display an About dialog box, send the [**ICM\_ABOUT**](icm-about.md) message (or use the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro).</span></span> <span data-ttu-id="972e3-114">Можно также отобразить диалоговое окно о программе программы сжатия или распаковки, отправив ICM \_ о сообщении и изменив значение параметра *wParam* (или с помощью макроса [**икабаут**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).</span><span class="sxs-lookup"><span data-stu-id="972e3-114">You can also display the About dialog box of a compressor or decompressor by sending the ICM\_ABOUT message and changing the value of the *wParam* parameter (or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro).</span></span>

 

 




