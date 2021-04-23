---
description: Метод Жетлангфромлангид извлекает удобную для восприятия строку при получении идентификатора основного языка.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Метод Жетлангфромлангид
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894666"
---
# <a name="getlangfromlangid-method"></a><span data-ttu-id="ea0ef-103">Метод Жетлангфромлангид</span><span class="sxs-lookup"><span data-stu-id="ea0ef-103">GetLangFromLangID Method</span></span>

> [!Note]  
> <span data-ttu-id="ea0ef-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ea0ef-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ea0ef-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="ea0ef-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ea0ef-106">`GetLangFromLangID`Метод получает строку, доступную для чтения, при наличии основного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="ea0ef-106">The `GetLangFromLangID` method retrieves a human-readable string when given a primary language ID.</span></span>

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a><span data-ttu-id="ea0ef-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea0ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea0ef-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*ипримарилангид*</span><span class="sxs-lookup"><span data-stu-id="ea0ef-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span></span>
</dt> <dd>

<span data-ttu-id="ea0ef-109">Указывает основной идентификатор языка в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="ea0ef-109">Specifies the primary language ID as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea0ef-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea0ef-110">Return Value</span></span>

<span data-ttu-id="ea0ef-111">Возвращает строковое представление языка, который может отображаться в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="ea0ef-111">Returns a String representation of the language that can be displayed in the application's user interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea0ef-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea0ef-112">Remarks</span></span>

<span data-ttu-id="ea0ef-113">Хотя этот метод называется `GetLangFromLangID` , передаваемый параметр фактически является основным идентификатором языка, а не идентификатором языка.</span><span class="sxs-lookup"><span data-stu-id="ea0ef-113">Although this method is named `GetLangFromLangID`, the parameter that you pass is actually the primary language ID, not the language ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea0ef-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea0ef-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea0ef-115">**жетаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="ea0ef-115">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> <dt>

[<span data-ttu-id="ea0ef-116">**жетдвдтекстлангуажелЦид**</span><span class="sxs-lookup"><span data-stu-id="ea0ef-116">**GetDVDTextLanguageLCID**</span></span>](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



