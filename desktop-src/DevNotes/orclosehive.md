---
description: Закрывает указанный куст автономного реестра и освобождает память, выделенную для Hive.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: Функция Орклосехиве (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649011"
---
# <a name="orclosehive-function"></a><span data-ttu-id="829bd-103">Функция Орклосехиве</span><span class="sxs-lookup"><span data-stu-id="829bd-103">ORCloseHive function</span></span>

<span data-ttu-id="829bd-104">Закрывает указанный куст автономного реестра и освобождает память, выделенную для Hive.</span><span class="sxs-lookup"><span data-stu-id="829bd-104">Closes the specified offline registry hive and frees memory allocated for the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="829bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="829bd-105">Syntax</span></span>


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="829bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="829bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="829bd-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="829bd-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="829bd-108">Маркер корневого ключа автономного куста реестра, который необходимо закрыть.</span><span class="sxs-lookup"><span data-stu-id="829bd-108">A handle to the root key of the offline registry hive to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="829bd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="829bd-109">Return value</span></span>

<span data-ttu-id="829bd-110">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="829bd-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="829bd-111">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="829bd-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="829bd-112">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="829bd-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="829bd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="829bd-113">Remarks</span></span>

<span data-ttu-id="829bd-114">Функция **орклосехиве** освобождает всю память, выделенную автономными функциями реестра от имени указанного Hive.</span><span class="sxs-lookup"><span data-stu-id="829bd-114">The **ORCloseHive** function frees all memory allocated by the offline registry functions on behalf of the specified hive.</span></span>

<span data-ttu-id="829bd-115">Чтобы сохранить изменения в Hive, вызовите функцию [**орсавехиве**](orsavehive.md) перед вызовом **орклосехиве**.</span><span class="sxs-lookup"><span data-stu-id="829bd-115">To preserve changes to the hive, call the [**ORSaveHive**](orsavehive.md) function before calling **ORCloseHive**.</span></span>

## <a name="requirements"></a><span data-ttu-id="829bd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="829bd-116">Requirements</span></span>



| <span data-ttu-id="829bd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="829bd-117">Requirement</span></span> | <span data-ttu-id="829bd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="829bd-118">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="829bd-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="829bd-119">Redistributable</span></span><br/> | <span data-ttu-id="829bd-120">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="829bd-120">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="829bd-121">Header</span><span class="sxs-lookup"><span data-stu-id="829bd-121">Header</span></span><br/>          | <dl> <span data-ttu-id="829bd-122"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="829bd-122"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="829bd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="829bd-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="829bd-124"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="829bd-124"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="829bd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="829bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829bd-126">**оропенхиве**</span><span class="sxs-lookup"><span data-stu-id="829bd-126">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="829bd-127">**орсавехиве**</span><span class="sxs-lookup"><span data-stu-id="829bd-127">**ORSaveHive**</span></span>](orsavehive.md)
</dt> </dl>

 

 
