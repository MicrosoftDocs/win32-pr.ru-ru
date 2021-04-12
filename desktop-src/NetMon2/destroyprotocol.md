---
description: Функция Дестройпротокол уничтожает протокол, создаваемый функцией Креатепротокол.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Функция Дестройпротокол (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264367"
---
# <a name="destroyprotocol-function"></a><span data-ttu-id="f6027-103">Функция Дестройпротокол</span><span class="sxs-lookup"><span data-stu-id="f6027-103">DestroyProtocol function</span></span>

<span data-ttu-id="f6027-104">Функция **дестройпротокол** уничтожает протокол, создаваемый функцией **креатепротокол** .</span><span class="sxs-lookup"><span data-stu-id="f6027-104">The **DestroyProtocol** function destroys the protocol that the **CreateProtocol** function creates.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6027-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6027-105">Syntax</span></span>


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="f6027-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6027-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6027-107">*хпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6027-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6027-108">Обработчик для уничтожения протокола.</span><span class="sxs-lookup"><span data-stu-id="f6027-108">Handle to the protocol to be destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6027-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6027-109">Return value</span></span>

<span data-ttu-id="f6027-110">Нет.</span><span class="sxs-lookup"><span data-stu-id="f6027-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6027-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="f6027-111">Remarks</span></span>

<span data-ttu-id="f6027-112">Библиотека DLL анализатора вызывает функцию **дестройпротокол** во время реализации [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="f6027-112">The parser DLL calls the **DestroyProtocol** function during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="f6027-113">**Дестройпротокол** вызывается, когда операционная система собирается выгрузить библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="f6027-113">**DestroyProtocol** is called when the operating system is going to unload the DLL.</span></span>



| <span data-ttu-id="f6027-114">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="f6027-114">For information on</span></span>                                        | <span data-ttu-id="f6027-115">См.</span><span class="sxs-lookup"><span data-stu-id="f6027-115">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f6027-116">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="f6027-116">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="f6027-117">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="f6027-117">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="f6027-118">Реализация функции **DllMain** включает пример.</span><span class="sxs-lookup"><span data-stu-id="f6027-118">How to implement **DllMain** includes an example.</span></span>         | [<span data-ttu-id="f6027-119">Реализация DllMain</span><span class="sxs-lookup"><span data-stu-id="f6027-119">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="f6027-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f6027-120">Requirements</span></span>



| <span data-ttu-id="f6027-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f6027-121">Requirement</span></span> | <span data-ttu-id="f6027-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f6027-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6027-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6027-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f6027-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6027-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f6027-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6027-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f6027-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6027-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f6027-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f6027-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6027-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6027-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f6027-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6027-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6027-130"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6027-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f6027-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f6027-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6027-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6027-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6027-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6027-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6027-134">DllMain</span><span class="sxs-lookup"><span data-stu-id="f6027-134">DllMain</span></span>](dllmain-parser.md)
</dt> </dl>

 

 




