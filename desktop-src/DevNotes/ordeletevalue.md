---
description: Удаляет именованное значение из указанного раздела реестра в автономном кусте реестра.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Функция Орделетевалуе (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669157"
---
# <a name="ordeletevalue-function"></a><span data-ttu-id="b6093-103">Функция Орделетевалуе</span><span class="sxs-lookup"><span data-stu-id="b6093-103">ORDeleteValue function</span></span>

<span data-ttu-id="b6093-104">Удаляет именованное значение из указанного раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="b6093-104">Removes a named value from the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6093-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6093-105">Syntax</span></span>


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a><span data-ttu-id="b6093-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6093-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6093-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6093-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6093-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="b6093-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="b6093-109">*лпвалуенаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b6093-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b6093-110">Удаляемое значение реестра.</span><span class="sxs-lookup"><span data-stu-id="b6093-110">The registry value to be removed.</span></span> <span data-ttu-id="b6093-111">Если этот параметр имеет **значение NULL** или является пустой строкой, то неименованное значение по умолчанию, заданное функцией [**орсетвалуе**](orsetvalue.md) , удаляется.</span><span class="sxs-lookup"><span data-stu-id="b6093-111">If this parameter is **NULL** or an empty string, the default unnamed value set by the [**ORSetValue**](orsetvalue.md) function is removed.</span></span>

<span data-ttu-id="b6093-112">В именах значений регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="b6093-112">Value names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6093-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6093-113">Return value</span></span>

<span data-ttu-id="b6093-114">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b6093-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b6093-115">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b6093-115">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="b6093-116">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="b6093-116">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6093-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b6093-117">Requirements</span></span>



| <span data-ttu-id="b6093-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b6093-118">Requirement</span></span> | <span data-ttu-id="b6093-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b6093-119">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6093-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b6093-120">Redistributable</span></span><br/> | <span data-ttu-id="b6093-121">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b6093-121">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="b6093-122">Header</span><span class="sxs-lookup"><span data-stu-id="b6093-122">Header</span></span><br/>          | <dl> <span data-ttu-id="b6093-123"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6093-123"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6093-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b6093-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="b6093-125"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6093-125"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6093-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6093-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6093-127">**орсетвалуе**</span><span class="sxs-lookup"><span data-stu-id="b6093-127">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
