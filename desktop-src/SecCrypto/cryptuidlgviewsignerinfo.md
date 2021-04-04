---
description: Отображает диалоговое окно, содержащее сведения о подписавшем для подписанного сообщения.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: Функция CryptUIDlgViewSignerInfo
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897078"
---
# <a name="cryptuidlgviewsignerinfo-function"></a><span data-ttu-id="f2927-103">Функция CryptUIDlgViewSignerInfo</span><span class="sxs-lookup"><span data-stu-id="f2927-103">CryptUIDlgViewSignerInfo function</span></span>

<span data-ttu-id="f2927-104">\[Функция **криптуидлгвиевсигнеринфо** доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f2927-104">\[The **CryptUIDlgViewSignerInfo** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f2927-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f2927-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f2927-106">\]</span><span class="sxs-lookup"><span data-stu-id="f2927-106">\]</span></span>

<span data-ttu-id="f2927-107">Функция **криптуидлгвиевсигнеринфо** отображает диалоговое окно, содержащее сведения о подписавшем для подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="f2927-107">The **CryptUIDlgViewSignerInfo** function displays a dialog box that contains the signer information for a signed message.</span></span>

> [!Note]  
> <span data-ttu-id="f2927-108">Эта функция не объявлена в опубликованном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="f2927-108">This function is not declared in a published header file.</span></span> <span data-ttu-id="f2927-109">Чтобы использовать эту структуру, объявите ее в точно указанном формате.</span><span class="sxs-lookup"><span data-stu-id="f2927-109">To use this structure, declare it in the exact format shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2927-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2927-110">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="f2927-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2927-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2927-112">*пквси* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2927-112">*pcvsi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2927-113">Указатель на структуру [**структуры динамической компоновки Cryptui \_ виевсигнеринфо \_**](cryptui-viewsignerinfo-struct.md) , которая содержит сведения о подписавшем для вывода.</span><span class="sxs-lookup"><span data-stu-id="f2927-113">A pointer to a [**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**](cryptui-viewsignerinfo-struct.md) structure that contains the signer information to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2927-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2927-114">Return value</span></span>

<span data-ttu-id="f2927-115">Эта функция возвращает ненулевое значение при успешном выполнении и ноль при сбое.</span><span class="sxs-lookup"><span data-stu-id="f2927-115">This function returns a nonzero value on success and zero on failure.</span></span> <span data-ttu-id="f2927-116">Для получения расширенных сведений об ошибках вызовите функцию [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f2927-116">For extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="f2927-117">Возможные коды ошибок, возвращаемые из [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) , включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="f2927-117">Possible error codes returned from [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f2927-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f2927-118">Return code</span></span>                                                                                   | <span data-ttu-id="f2927-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f2927-119">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="f2927-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f2927-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f2927-121">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="f2927-121">One or more arguments are not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="f2927-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f2927-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f2927-123">Ошибка при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="f2927-123">A memory allocation failure occurred.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="f2927-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f2927-124">Requirements</span></span>



| <span data-ttu-id="f2927-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f2927-125">Requirement</span></span> | <span data-ttu-id="f2927-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f2927-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2927-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2927-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f2927-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2927-128">Windows XP \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f2927-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2927-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f2927-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2927-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2927-131">Дата окончания поддержки</span><span class="sxs-lookup"><span data-stu-id="f2927-131">End of support</span></span><br/> | <span data-ttu-id="f2927-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f2927-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f2927-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2927-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2927-134"><dt>Динамической компоновки Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2927-134"><dt>Cryptui.lib</dt></span></span> </dl>      |
| <span data-ttu-id="f2927-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f2927-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2927-136"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2927-136"><dt>Cryptui.dll</dt></span></span> </dl>      |
| <span data-ttu-id="f2927-137">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f2927-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f2927-138">**Криптуидлгвиевсигнеринфов** (Юникод) и **криптуидлгвиевсигнеринфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f2927-138">**CryptUIDlgViewSignerInfoW** (Unicode) and **CryptUIDlgViewSignerInfoA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2927-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2927-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2927-140">**\_Структура ВИЕВСИГНЕРИНФО \_ динамической компоновки Cryptui**</span><span class="sxs-lookup"><span data-stu-id="f2927-140">**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**</span></span>](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
