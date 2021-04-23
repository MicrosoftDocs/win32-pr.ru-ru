---
description: Задает данные для значения указанного раздела реестра в автономном кусте реестра.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Функция Орсетвалуе (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649073"
---
# <a name="orsetvalue-function"></a><span data-ttu-id="6ce8c-103">Функция Орсетвалуе</span><span class="sxs-lookup"><span data-stu-id="6ce8c-103">ORSetValue function</span></span>

<span data-ttu-id="6ce8c-104">Задает данные для значения указанного раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-104">Sets the data for the value of a specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ce8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ce8c-105">Syntax</span></span>


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="6ce8c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ce8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ce8c-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ce8c-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce8c-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="6ce8c-109">*лпвалуенаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6ce8c-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce8c-110">Имя устанавливаемого значения.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-110">The name of the value to be set.</span></span> <span data-ttu-id="6ce8c-111">Если значение с таким именем еще не существует в ключе, функция добавляет его в ключ.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-111">If a value with this name is not already present in the key, the function adds it to the key.</span></span>

<span data-ttu-id="6ce8c-112">Если *лпвалуенаме* имеет **значение NULL** или является пустой строкой, функция задает тип и данные для безымянного или значения по умолчанию ключа.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-112">If *lpValueName* is **NULL** or an empty string, "", the function sets the type and data for the key's unnamed or default value.</span></span>

<span data-ttu-id="6ce8c-113">Дополнительные сведения см. в разделе [ограничения размера элементов реестра](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="6ce8c-113">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="6ce8c-114">Разделы реестра не имеют значений по умолчанию, но могут иметь одно безымянное значение, которое может быть любого типа.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-114">Registry keys do not have default values, but they can have one unnamed value, which can be of any type.</span></span>

</dd> <dt>

<span data-ttu-id="6ce8c-115">*двтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ce8c-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce8c-116">Тип данных, на который указывает параметр *лпдата* .</span><span class="sxs-lookup"><span data-stu-id="6ce8c-116">The type of data pointed to by the *lpData* parameter.</span></span> <span data-ttu-id="6ce8c-117">Список возможных типов см. в разделе [типы значений реестра](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="6ce8c-117">For a list of the possible types, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ce8c-118">*лпдата* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6ce8c-118">*lpData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce8c-119">Сохраняемые данные.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-119">The data to be stored.</span></span>

<span data-ttu-id="6ce8c-120">Для типов, основанных на строках, таких как REG \_ SZ, строка должна завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-120">For string-based types, such as REG\_SZ, the string must be null-terminated.</span></span> <span data-ttu-id="6ce8c-121">Для \_ \_ типа данных reg Multi SZ строка должна завершаться двумя символами NULL.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-121">For the REG\_MULTI\_SZ data type, the string must be terminated with two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="6ce8c-122">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ce8c-122">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce8c-123">Размер информации, на которую указывает параметр *лпдата* в байтах.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-123">The size of the information pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="6ce8c-124">Если данные имеют тип REG \_ SZ, REG \_ expand \_ SZ или REG \_ Multi \_ SZ, *cbData* должен включать размер завершающего нуль-символа или символов.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-124">If the data is of type REG\_SZ, REG\_EXPAND\_SZ, or REG\_MULTI\_SZ, *cbData* must include the size of the terminating null character or characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ce8c-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ce8c-125">Return value</span></span>

<span data-ttu-id="6ce8c-126">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="6ce8c-127">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-127">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="6ce8c-128">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-128">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ce8c-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ce8c-129">Remarks</span></span>

<span data-ttu-id="6ce8c-130">Размеры значений ограничены доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-130">Value sizes are limited by available memory.</span></span> <span data-ttu-id="6ce8c-131">Длинные значения (более 2048 байт) должны храниться в виде файлов с именами файлов, хранящимися в реестре.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-131">Long values (more than 2048 bytes) should be stored as files with the file names stored in the registry.</span></span> <span data-ttu-id="6ce8c-132">Это помогает реестру работать эффективно.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-132">This helps the registry perform efficiently.</span></span> <span data-ttu-id="6ce8c-133">Элементы приложения, такие как значки, точечные рисунки и исполняемые файлы, должны храниться в виде файлов и не помещаться в реестр.</span><span class="sxs-lookup"><span data-stu-id="6ce8c-133">Application elements such as icons, bitmaps, and executable files should be stored as files and not be placed in the registry.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ce8c-134">Требования</span><span class="sxs-lookup"><span data-stu-id="6ce8c-134">Requirements</span></span>



| <span data-ttu-id="6ce8c-135">Требование</span><span class="sxs-lookup"><span data-stu-id="6ce8c-135">Requirement</span></span> | <span data-ttu-id="6ce8c-136">Значение</span><span class="sxs-lookup"><span data-stu-id="6ce8c-136">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce8c-137">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6ce8c-137">Redistributable</span></span><br/> | <span data-ttu-id="6ce8c-138">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="6ce8c-138">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="6ce8c-139">Header</span><span class="sxs-lookup"><span data-stu-id="6ce8c-139">Header</span></span><br/>          | <dl> <span data-ttu-id="6ce8c-140"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ce8c-140"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ce8c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6ce8c-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="6ce8c-142"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ce8c-142"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ce8c-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ce8c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ce8c-144">**оркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="6ce8c-144">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="6ce8c-145">**оропенкэй**</span><span class="sxs-lookup"><span data-stu-id="6ce8c-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
