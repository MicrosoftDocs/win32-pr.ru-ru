---
title: Иажентбаллун Жетфонтундерлине
description: Иажентбаллун Жетфонтундерлине
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068561"
---
# <a name="iagentballoongetfontunderline"></a><span data-ttu-id="b5f16-103">Иажентбаллун:: Жетфонтундерлине</span><span class="sxs-lookup"><span data-stu-id="b5f16-103">IAgentBalloon::GetFontUnderline</span></span>

<span data-ttu-id="b5f16-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b5f16-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

<span data-ttu-id="b5f16-105">Указывает, установлен ли стиль подчеркивания для шрифта, используемого в тексте всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="b5f16-105">Indicates whether the font used in a word balloon has the underline style set.</span></span>

-   <span data-ttu-id="b5f16-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b5f16-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b5f16-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*пбфонтундерлине*</span><span class="sxs-lookup"><span data-stu-id="b5f16-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span></span>
</dt> <dd>

<span data-ttu-id="b5f16-108">Адрес значения, которое принимает значение **true** , если задан стиль подчеркивания шрифта, и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b5f16-108">The address of a value that receives **True** if the font underline style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="b5f16-109">Стиль шрифта, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b5f16-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="b5f16-110">Оно не может быть изменено приложением.</span><span class="sxs-lookup"><span data-stu-id="b5f16-110">It cannot be changed by an application.</span></span> <span data-ttu-id="b5f16-111">Однако пользователь может переопределить параметры шрифта для всех символов с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b5f16-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




