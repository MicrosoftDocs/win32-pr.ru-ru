---
description: Функция Креатепротокол сообщает сетевой монитор о существовании определенного средства синтаксического анализа протокола.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Функция Креатепротокол (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156703"
---
# <a name="createprotocol-function"></a><span data-ttu-id="03593-103">Функция Креатепротокол</span><span class="sxs-lookup"><span data-stu-id="03593-103">CreateProtocol function</span></span>

<span data-ttu-id="03593-104">Функция **креатепротокол** сообщает сетевой монитор о существовании определенного средства синтаксического анализа протокола.</span><span class="sxs-lookup"><span data-stu-id="03593-104">The **CreateProtocol** function notifies Network Monitor that a specific protocol parser exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="03593-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03593-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a><span data-ttu-id="03593-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03593-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03593-107">*ProtocolName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03593-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03593-108">Имя протокола, который будет обнаружен анализатором.</span><span class="sxs-lookup"><span data-stu-id="03593-108">Name of the protocol the parser will detect.</span></span>

</dd> <dt>

<span data-ttu-id="03593-109">*лпентрипоинтс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03593-109">*lpEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03593-110">Структура [EntryPoint](entrypoints.md) , содержащая остальные точки входа DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="03593-110">An [ENTRYPOINTS](entrypoints.md) structure that contains the remaining parser DLL entry points.</span></span> <span data-ttu-id="03593-111">Список функций экспорта, на которые ссылается каждая точка входа, см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="03593-111">See Remarks for a list of the export functions that each entry point references.</span></span> <span data-ttu-id="03593-112">Точки входа должны быть предоставлены в том порядке, в каком структура **EntryPoint** указывает.</span><span class="sxs-lookup"><span data-stu-id="03593-112">Entry points must be provided in the order that the **ENTRYPOINTS** structure specifies.</span></span>

</dd> <dt>

<span data-ttu-id="03593-113">*кбентрипоинтс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03593-113">*cbEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03593-114">Размер структуры **EntryPoint** .</span><span class="sxs-lookup"><span data-stu-id="03593-114">The size of the **ENTRYPOINTS** structure.</span></span> <span data-ttu-id="03593-115">Сетевой монитор предоставляет макрос ENTRYPOINT \_ size, который можно использовать для указания размера структуры.</span><span class="sxs-lookup"><span data-stu-id="03593-115">Network Monitor provides an ENTRYPOINTS\_SIZE macro that you can use to specify the size of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03593-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03593-116">Return value</span></span>

<span data-ttu-id="03593-117">Если функция выполнена успешно, возвращаемое значение является маркером протокола.</span><span class="sxs-lookup"><span data-stu-id="03593-117">If the function is successful, the return value is a handle to the protocol.</span></span>

<span data-ttu-id="03593-118">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="03593-118">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03593-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03593-119">Remarks</span></span>

<span data-ttu-id="03593-120">Библиотека DLL средства синтаксического анализа вызывает **креатепротокол** во время реализации [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="03593-120">The parser DLL calls **CreateProtocol** during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="03593-121">Функция **креатепротокол** вызывается, когда операционная система ЗАГРУЖАЕТ библиотеку DLL средства синтаксического анализа в первый раз.</span><span class="sxs-lookup"><span data-stu-id="03593-121">The **CreateProtocol** function is called when the operating system loads the parser DLL for the first time.</span></span>

<span data-ttu-id="03593-122">Точки входа, на которые ссылается параметр *лпентрипоинтс* , включают указатели на следующие функции экспорта, которые должны быть представлены в указанном здесь порядке.</span><span class="sxs-lookup"><span data-stu-id="03593-122">The entry points referenced in the *lpEntryPoints* parameter include pointers to the following export functions that must be provided in the order presented here.</span></span>

-   [<span data-ttu-id="03593-123">Зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="03593-123">Register</span></span>](register-parser.md)
-   [<span data-ttu-id="03593-124">Отмена регистрации</span><span class="sxs-lookup"><span data-stu-id="03593-124">Deregister</span></span>](deregister.md)
-   [<span data-ttu-id="03593-125">рекогнизефраме</span><span class="sxs-lookup"><span data-stu-id="03593-125">RecognizeFrame</span></span>](recognizeframe.md)
-   [<span data-ttu-id="03593-126">аттачпропертиес</span><span class="sxs-lookup"><span data-stu-id="03593-126">AttachProperties</span></span>](attachproperties.md)
-   [<span data-ttu-id="03593-127">форматпропертиес</span><span class="sxs-lookup"><span data-stu-id="03593-127">FormatProperties</span></span>](formatproperties.md)



| <span data-ttu-id="03593-128">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="03593-128">For information on</span></span>                                                                                 | <span data-ttu-id="03593-129">См.</span><span class="sxs-lookup"><span data-stu-id="03593-129">See</span></span>                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="03593-130">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="03593-130">What parsers are, and how they work with Network Monitor.</span></span>                                          | [<span data-ttu-id="03593-131">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="03593-131">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="03593-132">Реализация функции **DllMain** включает в себя пример вызова **креатепротокол** в **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="03593-132">How to implement **DllMain** includes an example of calling **CreateProtocol** within **DllMain**.</span></span> | [<span data-ttu-id="03593-133">Реализация DllMain</span><span class="sxs-lookup"><span data-stu-id="03593-133">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="03593-134">Требования</span><span class="sxs-lookup"><span data-stu-id="03593-134">Requirements</span></span>



| <span data-ttu-id="03593-135">Требование</span><span class="sxs-lookup"><span data-stu-id="03593-135">Requirement</span></span> | <span data-ttu-id="03593-136">Значение</span><span class="sxs-lookup"><span data-stu-id="03593-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="03593-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03593-137">Minimum supported client</span></span><br/> | <span data-ttu-id="03593-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="03593-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="03593-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03593-139">Minimum supported server</span></span><br/> | <span data-ttu-id="03593-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="03593-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="03593-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="03593-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="03593-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="03593-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="03593-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03593-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="03593-144"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03593-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="03593-145">DLL</span><span class="sxs-lookup"><span data-stu-id="03593-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03593-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03593-146"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03593-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03593-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03593-148">DllMain</span><span class="sxs-lookup"><span data-stu-id="03593-148">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

