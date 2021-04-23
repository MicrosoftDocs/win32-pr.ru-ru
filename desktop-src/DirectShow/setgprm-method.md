---
description: Метод Сетгпрм задает указанное значение для указанного общего параметра Register.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Метод Сетгпрм
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682226"
---
# <a name="setgprm-method"></a><span data-ttu-id="06b33-103">Метод Сетгпрм</span><span class="sxs-lookup"><span data-stu-id="06b33-103">SetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="06b33-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="06b33-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="06b33-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="06b33-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="06b33-106">`SetGPRM`Метод задает указанное значение для регистра общих параметров.</span><span class="sxs-lookup"><span data-stu-id="06b33-106">The `SetGPRM` method sets the specified general parameter register to the specified value.</span></span>

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a><span data-ttu-id="06b33-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="06b33-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b33-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*ииндекс*</span><span class="sxs-lookup"><span data-stu-id="06b33-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="06b33-109">Задает регистр общего параметра для задания в качестве целого числа.</span><span class="sxs-lookup"><span data-stu-id="06b33-109">Specifies the general parameter register to set as an Integer.</span></span> <span data-ttu-id="06b33-110">Целочисленное значение должно находиться в диапазоне от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="06b33-110">The Integer value must range from 0 through 15.</span></span>

</dd> <dt>

<span data-ttu-id="06b33-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*Nзначение*</span><span class="sxs-lookup"><span data-stu-id="06b33-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*</span></span>
</dt> <dd>

<span data-ttu-id="06b33-112">Задает новое значение для регистра в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="06b33-112">Specifies the new value for the register as an Integer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06b33-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06b33-113">Remarks</span></span>

<span data-ttu-id="06b33-114">Общие регистры параметров, или Гпрмс, представляют собой 16-битные регистры, которые каждый диск может использовать уникальным образом для временного хранения данных.</span><span class="sxs-lookup"><span data-stu-id="06b33-114">General parameter registers, or GPRMs, are 16-bit registers that each disc can use in unique ways for temporary data storage.</span></span> <span data-ttu-id="06b33-115">Приложению проигрывателя не требуется доступ к этим регистрам для любого стандартного элемента управления воспроизведением или навигации с помощью объекта **мсвебдвд** .</span><span class="sxs-lookup"><span data-stu-id="06b33-115">A player application does not need to access these registers for any standard playback or navigation control using the **MSWebDVD** object.</span></span> <span data-ttu-id="06b33-116">Этот метод предоставляется для приложений проигрывателя, реализующих расширенные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="06b33-116">This method is provided for player applications implementing advanced functionality.</span></span> <span data-ttu-id="06b33-117">Не пытайтесь изменить Гпрмс напрямую, если вы не имеете исчерпывающих знаний о спецификации DVD и способы, с помощью которых Гпрмс используется на конкретном диске для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="06b33-117">Do not attempt to modify the GPRMs directly unless you have a thorough knowledge of the DVD specification and the ways in which the GPRMs are used on the particular disc to be played.</span></span> <span data-ttu-id="06b33-118">Изменение этих значений может привести к непредсказуемому поведению.</span><span class="sxs-lookup"><span data-stu-id="06b33-118">Changing these values can result in unpredictable behavior.</span></span>

 

 



