---
title: Иажентбаллун Жетфонтстрикесру
description: Иажентбаллун Жетфонтстрикесру
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411358"
---
# <a name="iagentballoongetfontstrikethru"></a><span data-ttu-id="e3019-103">Иажентбаллун:: Жетфонтстрикесру</span><span class="sxs-lookup"><span data-stu-id="e3019-103">IAgentBalloon::GetFontStrikethru</span></span>

<span data-ttu-id="e3019-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3019-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

<span data-ttu-id="e3019-105">Указывает, задан ли стиль перечеркивания для шрифта, используемого в тексте всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="e3019-105">Indicates whether the font used in a word balloon has the strikethrough style set.</span></span>

-   <span data-ttu-id="e3019-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e3019-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e3019-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*пбфонтстрикесру*</span><span class="sxs-lookup"><span data-stu-id="e3019-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span></span>
</dt> <dd>

<span data-ttu-id="e3019-108">Адрес значения, которое принимает значение **true** , если задан стиль перечеркивания шрифта, и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e3019-108">The address of a value that receives **True** if the font strikethrough style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="e3019-109">Стиль шрифта, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e3019-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e3019-110">Оно не может быть изменено приложением.</span><span class="sxs-lookup"><span data-stu-id="e3019-110">It cannot be changed by an application.</span></span> <span data-ttu-id="e3019-111">Однако пользователь может переопределить параметры шрифта для всех символов с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e3019-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




