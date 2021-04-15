---
description: Создает автономный куст реестра, содержащий один пустой корневой ключ.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Функция Оркреатехиве (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649010"
---
# <a name="orcreatehive-function"></a><span data-ttu-id="9115c-103">Функция Оркреатехиве</span><span class="sxs-lookup"><span data-stu-id="9115c-103">ORCreateHive function</span></span>

<span data-ttu-id="9115c-104">Создает автономный куст реестра, содержащий один пустой корневой ключ.</span><span class="sxs-lookup"><span data-stu-id="9115c-104">Creates an offline registry hive that contains a single empty root key.</span></span>

## <a name="syntax"></a><span data-ttu-id="9115c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9115c-105">Syntax</span></span>


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="9115c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9115c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9115c-107">*фкресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9115c-107">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9115c-108">Указывает на переменную для получения маркера корневого ключа только что созданного автономного куста реестра.</span><span class="sxs-lookup"><span data-stu-id="9115c-108">Points to a variable to receive a handle to the root key of the newly created offline registry hive.</span></span> <span data-ttu-id="9115c-109">Если не удается создать куст, функция присваивает этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9115c-109">If the hive cannot be created, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9115c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9115c-110">Return value</span></span>

<span data-ttu-id="9115c-111">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9115c-111">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9115c-112">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9115c-112">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="9115c-113">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="9115c-113">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="9115c-114">Если недостаточно памяти для создания куста реестра, функция возвращает ошибку \_ \_ недостаточно \_ памяти.</span><span class="sxs-lookup"><span data-stu-id="9115c-114">If there is insufficient memory to create the registry hive, the function returns ERROR\_NOT\_ENOUGH\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9115c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9115c-115">Remarks</span></span>

<span data-ttu-id="9115c-116">Функция **оркреатехиве** создает пустой куст автономного реестра в памяти.</span><span class="sxs-lookup"><span data-stu-id="9115c-116">The **ORCreateHive** function creates an empty offline registry hive in memory.</span></span> <span data-ttu-id="9115c-117">Используйте функции [**оркреатекэй**](orcreatekey.md) и [**орсетвалуе**](orsetvalue.md) , чтобы добавить ключи и задать их значения.</span><span class="sxs-lookup"><span data-stu-id="9115c-117">Use the [**ORCreateKey**](orcreatekey.md) and [**ORSetValue**](orsetvalue.md) functions to add keys and set their values.</span></span>

## <a name="requirements"></a><span data-ttu-id="9115c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9115c-118">Requirements</span></span>



| <span data-ttu-id="9115c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9115c-119">Requirement</span></span> | <span data-ttu-id="9115c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9115c-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9115c-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9115c-121">Redistributable</span></span><br/> | <span data-ttu-id="9115c-122">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="9115c-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="9115c-123">Header</span><span class="sxs-lookup"><span data-stu-id="9115c-123">Header</span></span><br/>          | <dl> <span data-ttu-id="9115c-124"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="9115c-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="9115c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9115c-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="9115c-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9115c-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9115c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9115c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9115c-128">**оркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="9115c-128">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="9115c-129">**оропенхиве**</span><span class="sxs-lookup"><span data-stu-id="9115c-129">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="9115c-130">**орсавехиве**</span><span class="sxs-lookup"><span data-stu-id="9115c-130">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="9115c-131">**орсетвалуе**</span><span class="sxs-lookup"><span data-stu-id="9115c-131">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
