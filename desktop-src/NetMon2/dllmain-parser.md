---
description: Функция экспорта DllMain для средства синтаксического анализа определяет существование средства синтаксического анализа и освобождает ресурсы, которые сетевой монитор использует для анализатора. Функция DllMain должна быть реализована во всех библиотеках DLL средства синтаксического анализа.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Функция обратного вызова средства синтаксического анализа DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663639"
---
# <a name="dllmain-parser-callback-function"></a><span data-ttu-id="a36d1-104">Функция обратного вызова средства синтаксического анализа DllMain</span><span class="sxs-lookup"><span data-stu-id="a36d1-104">DllMain Parser callback function</span></span>

<span data-ttu-id="a36d1-105">Функция экспорта **DllMain** для средства синтаксического анализа определяет существование средства синтаксического анализа и освобождает ресурсы, которые сетевой монитор использует для анализатора.</span><span class="sxs-lookup"><span data-stu-id="a36d1-105">The **DllMain** export function for the parser identifies the existence of the parser, and releases resources that Network Monitor uses for the parser.</span></span> <span data-ttu-id="a36d1-106">Функция **DllMain** должна быть реализована во всех библиотеках DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="a36d1-106">**DllMain** must be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="a36d1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a36d1-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="a36d1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a36d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a36d1-109">*HINSTANCE* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a36d1-109">*hInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a36d1-110">Обработчик для экземпляра средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="a36d1-110">Handle to an instance of the parser.</span></span>

</dd> <dt>

<span data-ttu-id="a36d1-111">*Команда* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a36d1-111">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a36d1-112">Индикатор для определения причины вызова функции.</span><span class="sxs-lookup"><span data-stu-id="a36d1-112">Indicator to determine why the function is called.</span></span> <span data-ttu-id="a36d1-113">Список всех возможных флагов см. в разделе [DllMain](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="a36d1-113">For a list of all possible flags, see [DllMain](/windows/desktop/Dlls/dllmain).</span></span> <span data-ttu-id="a36d1-114">Реализация средства синтаксического анализа должна обрабатывать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="a36d1-114">The parser implementation must process the following values.</span></span>



| <span data-ttu-id="a36d1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a36d1-115">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="a36d1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a36d1-116">Meaning</span></span>                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <span data-ttu-id="a36d1-117"><dt>**\_Подключение к ПРОЦЕССУ DLL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a36d1-117"><dt>**DLL\_PROCESS\_ATTACH**</dt></span></span> </dl> | <span data-ttu-id="a36d1-118">При первом вызове функции **DllMain** библиотека DLL должна вызвать [креатепротокол](createprotocol.md) , чтобы предоставить сведения для сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="a36d1-118">When **DllMain** is called for the first time, the DLL must call [CreateProtocol](createprotocol.md) to provide information to Network Monitor.</span></span> <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <span data-ttu-id="a36d1-119"><dt>**\_отсоединение процесса DLL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a36d1-119"><dt>**DLL\_PROCESS\_DETACH**</dt></span></span> </dl> | <span data-ttu-id="a36d1-120">Когда функция **DllMain** вызывается в последний раз, Библиотека DLL должна вызвать [дестройпротокол](destroyprotocol.md) для освобождения ресурсов, используемых библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="a36d1-120">When **DllMain** is called for the last time, the DLL must call [DestroyProtocol](destroyprotocol.md) to release the resources that the DLL uses.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="a36d1-121">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="a36d1-121">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="a36d1-122">Сейчас не используется.</span><span class="sxs-lookup"><span data-stu-id="a36d1-122">Not used now.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a36d1-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a36d1-123">Return value</span></span>

<span data-ttu-id="a36d1-124">Библиотека DLL средства синтаксического анализа всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a36d1-124">The parser DLL always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a36d1-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a36d1-125">Remarks</span></span>

<span data-ttu-id="a36d1-126">Операционная система вызывает функцию **DllMain** для загрузки и выгрузки библиотеки DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="a36d1-126">The operating system calls **DllMain** to load and unload the parser DLL.</span></span> <span data-ttu-id="a36d1-127">Эта функция основана на функции [DllMain](/windows/desktop/Dlls/dllmain) библиотеки динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="a36d1-127">This function is based on the dynamic-link library [DllMain](/windows/desktop/Dlls/dllmain) function.</span></span>

<span data-ttu-id="a36d1-128">Также можно использовать реализацию функции **DllMain** для хранения экземпляра средства синтаксического анализа, который будет использоваться в будущем.</span><span class="sxs-lookup"><span data-stu-id="a36d1-128">You can also use the implementation of **DllMain** to store an instance of a parser for use in the future.</span></span> <span data-ttu-id="a36d1-129">Например, можно сохранить экземпляр библиотеки DLL средства синтаксического анализа, а затем использовать его для системного вызова в будущем.</span><span class="sxs-lookup"><span data-stu-id="a36d1-129">For example, you can store a parser DLL instance, and then use it for a system call in the future.</span></span>



| <span data-ttu-id="a36d1-130">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="a36d1-130">For information on</span></span>                                        | <span data-ttu-id="a36d1-131">См.</span><span class="sxs-lookup"><span data-stu-id="a36d1-131">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a36d1-132">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="a36d1-132">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="a36d1-133">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="a36d1-133">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="a36d1-134">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="a36d1-134">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="a36d1-135">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="a36d1-135">Parser DLL Architecture</span></span>](parser-dll-architecture.md)  |
| <span data-ttu-id="a36d1-136">Реализация функции **DllMain**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="a36d1-136">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="a36d1-137">Реализация DllMain</span><span class="sxs-lookup"><span data-stu-id="a36d1-137">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="a36d1-138">Требования</span><span class="sxs-lookup"><span data-stu-id="a36d1-138">Requirements</span></span>



| <span data-ttu-id="a36d1-139">Требование</span><span class="sxs-lookup"><span data-stu-id="a36d1-139">Requirement</span></span> | <span data-ttu-id="a36d1-140">Значение</span><span class="sxs-lookup"><span data-stu-id="a36d1-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a36d1-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a36d1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a36d1-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a36d1-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a36d1-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a36d1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a36d1-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a36d1-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a36d1-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a36d1-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a36d1-146"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="a36d1-146"><dt>Process.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a36d1-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a36d1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a36d1-148">креатепротокол</span><span class="sxs-lookup"><span data-stu-id="a36d1-148">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="a36d1-149">дестройпротокол</span><span class="sxs-lookup"><span data-stu-id="a36d1-149">DestroyProtocol</span></span>](destroyprotocol.md)
</dt> <dt>

[<span data-ttu-id="a36d1-150">DllMain</span><span class="sxs-lookup"><span data-stu-id="a36d1-150">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

