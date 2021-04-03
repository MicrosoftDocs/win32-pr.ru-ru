---
title: Раздел области
description: Раздел области
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, области
- обложки, области
- Создание обложек, раздел области
- Написание кода для обложек, раздел области
- области в обложках, раздел бегущей строки
- файлы определения обложки, раздел бегущей строки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780054"
---
# <a name="marquee-section"></a><span data-ttu-id="541c2-109">Раздел области</span><span class="sxs-lookup"><span data-stu-id="541c2-109">Marquee Section</span></span>

<span data-ttu-id="541c2-110">Раздел бегущая строка содержит сведения о текстовом поле бегущая строка, в котором будет отображаться бегущая строка:</span><span class="sxs-lookup"><span data-stu-id="541c2-110">The Marquee section contains information about the marquee text box, which will display scrolling text:</span></span>


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



<span data-ttu-id="541c2-111">Будет отображен заголовок и автор текущего элемента мультимедиа, хотя в области можно отобразить любой текстовый тип.</span><span class="sxs-lookup"><span data-stu-id="541c2-111">This will display the title and author of the current media item although you can display any text type in the marquee.</span></span> <span data-ttu-id="541c2-112">Например, можно также включить в бегущую строку имя файла, состояние и список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="541c2-112">For example, you could also include Filename, Status, and Playlist in your marquee.</span></span>

> [!Note]  
> <span data-ttu-id="541c2-113">Для обеспечения совместимости с версиями проигрывателя Windows Media Mobile, более ранними, чем проигрыватель Windows Media 10 Mobile, использование "Маркуис" в файле определения обложки по-прежнему считается действительным.</span><span class="sxs-lookup"><span data-stu-id="541c2-113">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="541c2-114">Дополнительные сведения см. в разделе [область](marquee.md) в справочнике по обложкам.</span><span class="sxs-lookup"><span data-stu-id="541c2-114">For more about the Marquee section, see [Marquee](marquee.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="541c2-115">См. также</span><span class="sxs-lookup"><span data-stu-id="541c2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="541c2-116">**Написание кода**</span><span class="sxs-lookup"><span data-stu-id="541c2-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




