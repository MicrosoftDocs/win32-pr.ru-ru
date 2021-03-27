---
description: Преобразует строку в идентификатор GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: Функция Гуидфромстринг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909556"
---
# <a name="guidfromstring-function"></a><span data-ttu-id="0daaa-103">Функция Гуидфромстринг</span><span class="sxs-lookup"><span data-stu-id="0daaa-103">GUIDFromString function</span></span>

<span data-ttu-id="0daaa-104">\[**Гуидфромстринг** доступен в Windows XP с пакетом обновления 2 (SP2) или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0daaa-104">\[**GUIDFromString** is available through Windows XP with Service Pack 2 (SP2) or Windows Vista.</span></span> <span data-ttu-id="0daaa-105">Он может быть изменен или недоступен в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="0daaa-105">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0daaa-106">Приложения должны использовать [**клсидфромстринг**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) или [**иидфромстринг**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) вместо этой функции.\]</span><span class="sxs-lookup"><span data-stu-id="0daaa-106">Applications should use [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) or [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) in place of this function.\]</span></span>

<span data-ttu-id="0daaa-107">Преобразует строку в идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="0daaa-107">Converts a string to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="0daaa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0daaa-108">Syntax</span></span>


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a><span data-ttu-id="0daaa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0daaa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0daaa-110">*ПСЗ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0daaa-110">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaa-111">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="0daaa-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="0daaa-112">Указатель на строку, завершающуюся нулем, для преобразования.</span><span class="sxs-lookup"><span data-stu-id="0daaa-112">A pointer to the null-terminated string to convert.</span></span> <span data-ttu-id="0daaa-113">Строка должна иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="0daaa-113">The string should be in the following form:</span></span>

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

<span data-ttu-id="0daaa-114">*пгуид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0daaa-114">*pguid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaa-115">Тип: **лпгуид**</span><span class="sxs-lookup"><span data-stu-id="0daaa-115">Type: **LPGUID**</span></span>

<span data-ttu-id="0daaa-116">Указатель на буфер для получения идентификатора GUID при возврате из метода.</span><span class="sxs-lookup"><span data-stu-id="0daaa-116">Pointer to a buffer to receive the GUID when this method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0daaa-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0daaa-117">Return value</span></span>

<span data-ttu-id="0daaa-118">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="0daaa-118">Type: **BOOL**</span></span>

<span data-ttu-id="0daaa-119">**Значение true** , если GUID был успешно создан; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0daaa-119">**TRUE** if the GUID was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0daaa-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="0daaa-120">Remarks</span></span>

<span data-ttu-id="0daaa-121">Эта функция не объявлена в заголовке или экспортируется по имени из DLL-файла.</span><span class="sxs-lookup"><span data-stu-id="0daaa-121">This function is not declared in a header or exported by name from a .dll file.</span></span> <span data-ttu-id="0daaa-122">Он должен быть загружен с Shell32.dll как порядковый номер 703 для **гуидфромстринга** и порядковый номер 704 для **гуидфромстрингв**.</span><span class="sxs-lookup"><span data-stu-id="0daaa-122">It must be loaded from Shell32.dll as ordinal 703 for **GUIDFromStringA** and ordinal 704 for **GUIDFromStringW**.</span></span>

<span data-ttu-id="0daaa-123">К нему также можно получить доступ из Shlwapi.dll как порядковый номер 269 для **гуидфромстринга** и порядковый номер 270 для **гуидфромстрингв**.</span><span class="sxs-lookup"><span data-stu-id="0daaa-123">It can also be accessed from Shlwapi.dll as ordinal 269 for **GUIDFromStringA** and ordinal 270 for **GUIDFromStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0daaa-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0daaa-124">Requirements</span></span>



| <span data-ttu-id="0daaa-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0daaa-125">Requirement</span></span> | <span data-ttu-id="0daaa-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0daaa-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0daaa-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0daaa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0daaa-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0daaa-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0daaa-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0daaa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0daaa-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0daaa-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0daaa-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0daaa-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0daaa-132"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0daaa-132"><dt>Shell32.dll</dt></span></span> </dl> |
| <span data-ttu-id="0daaa-133">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="0daaa-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0daaa-134">**Гуидфромстрингв** (Юникод) и **гуидфромстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0daaa-134">**GUIDFromStringW** (Unicode) and **GUIDFromStringA** (ANSI)</span></span><br/>                |



 

 
