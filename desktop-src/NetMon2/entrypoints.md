---
description: Структура ENTRYPOINT определяет точки входа для функций экспорта, которые сетевой монитор используют для работы средства синтаксического анализа.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: Структура ENTRYPOINT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990919"
---
# <a name="entrypoints-structure"></a><span data-ttu-id="0d480-103">Структура ENTRYPOINT</span><span class="sxs-lookup"><span data-stu-id="0d480-103">ENTRYPOINTS structure</span></span>

<span data-ttu-id="0d480-104">Структура **EntryPoint** определяет точки входа для функций экспорта, которые сетевой монитор используют для работы средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="0d480-104">The **ENTRYPOINTS** structure defines the entry points to the export functions that Network Monitor uses to operate the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d480-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d480-105">Syntax</span></span>


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a><span data-ttu-id="0d480-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0d480-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d480-107">**Зарегистрировать**</span><span class="sxs-lookup"><span data-stu-id="0d480-107">**Register**</span></span>
</dt> <dd>

<span data-ttu-id="0d480-108">Указатель на реализацию функции [*регистрации экспертов*](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="0d480-108">Pointer to the implementation of the [*Register expert*](register-expert.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0d480-109">**Отмена регистрации**</span><span class="sxs-lookup"><span data-stu-id="0d480-109">**Deregister**</span></span>
</dt> <dd>

<span data-ttu-id="0d480-110">Указатель на реализацию функции [**дерегистрации**](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="0d480-110">Pointer to the implementation of the [**Deregister**](deregister.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0d480-111">**рекогнизефраме**</span><span class="sxs-lookup"><span data-stu-id="0d480-111">**RecognizeFrame**</span></span>
</dt> <dd>

<span data-ttu-id="0d480-112">Указатель на реализацию функции экспорта [**рекогнизефраме**](recognizeframe.md) .</span><span class="sxs-lookup"><span data-stu-id="0d480-112">Pointer to the implementation of the [**RecognizeFrame**](recognizeframe.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="0d480-113">**аттачпропертиес**</span><span class="sxs-lookup"><span data-stu-id="0d480-113">**AttachProperties**</span></span>
</dt> <dd>

<span data-ttu-id="0d480-114">Указатель на реализацию функции экспорта [**аттачпропертиес**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="0d480-114">Pointer to the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="0d480-115">**форматпропертиес**</span><span class="sxs-lookup"><span data-stu-id="0d480-115">**FormatProperties**</span></span>
</dt> <dd>

<span data-ttu-id="0d480-116">Указатель на реализацию функции экспорта [**форматпропертиес**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="0d480-116">Pointer to the implementation of the [**FormatProperties**](formatproperties.md) export function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d480-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d480-117">Remarks</span></span>

<span data-ttu-id="0d480-118">Функция **креатепротокол** использует структуру **EntryPoint** для предоставления указателей на сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="0d480-118">The **CreateProtocol** function uses the **ENTRYPOINTS** structure to provide pointers to Network Monitor.</span></span> <span data-ttu-id="0d480-119">Указатели должны быть указаны в порядке, указанном в разделе предыдущие элементы.</span><span class="sxs-lookup"><span data-stu-id="0d480-119">The pointers must be specified in the order identified in the previous Members section.</span></span>

<span data-ttu-id="0d480-120">Функцию [**форматпропертиес**](formatproperties.md) не нужно реализовывать, если сетевой монитор не будет отображать данные протокола.</span><span class="sxs-lookup"><span data-stu-id="0d480-120">The [**FormatProperties**](formatproperties.md) function does not need to be implemented if Network Monitor will never display the protocol data.</span></span> <span data-ttu-id="0d480-121">Например, **форматпропертиес** не требуется реализовывать, если приложение экспорта использует выходные данные средства синтаксического анализа, а сетевой монитор не отображает выходные данные.</span><span class="sxs-lookup"><span data-stu-id="0d480-121">For example, **FormatProperties** does not need to be implemented if an export application uses the output from the parser, and Network Monitor does not display the output.</span></span>



| <span data-ttu-id="0d480-122">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="0d480-122">For information on</span></span>                                        | <span data-ttu-id="0d480-123">См.</span><span class="sxs-lookup"><span data-stu-id="0d480-123">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0d480-124">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="0d480-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="0d480-125">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="0d480-125">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="0d480-126">Реализация функции **DllMain**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="0d480-126">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="0d480-127">Реализация DllMain</span><span class="sxs-lookup"><span data-stu-id="0d480-127">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="0d480-128">Требования</span><span class="sxs-lookup"><span data-stu-id="0d480-128">Requirements</span></span>



| <span data-ttu-id="0d480-129">Требование</span><span class="sxs-lookup"><span data-stu-id="0d480-129">Requirement</span></span> | <span data-ttu-id="0d480-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0d480-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d480-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d480-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0d480-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d480-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0d480-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d480-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0d480-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d480-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d480-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0d480-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d480-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d480-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d480-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d480-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d480-138">аттачпропертиес</span><span class="sxs-lookup"><span data-stu-id="0d480-138">AttachProperties</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="0d480-139">креатепротокол</span><span class="sxs-lookup"><span data-stu-id="0d480-139">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="0d480-140">Отмена регистрации</span><span class="sxs-lookup"><span data-stu-id="0d480-140">Deregister</span></span>](deregister.md)
</dt> <dt>

[<span data-ttu-id="0d480-141">форматпропертиес</span><span class="sxs-lookup"><span data-stu-id="0d480-141">FormatProperties</span></span>](formatproperties.md)
</dt> <dt>

[<span data-ttu-id="0d480-142">рекогнизефраме</span><span class="sxs-lookup"><span data-stu-id="0d480-142">RecognizeFrame</span></span>](recognizeframe.md)
</dt> <dt>

[<span data-ttu-id="0d480-143">Зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="0d480-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




