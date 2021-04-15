---
description: Закрывает маркер указанного раздела реестра в автономном кусте реестра.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: Функция Орклосекэй (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: df6b8d9176efc1eb1e4ffb4e0453ec665ec19b6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669160"
---
# <a name="orclosekey-function"></a><span data-ttu-id="7ac0b-103">Функция Орклосекэй</span><span class="sxs-lookup"><span data-stu-id="7ac0b-103">ORCloseKey function</span></span>

<span data-ttu-id="7ac0b-104">Закрывает маркер указанного раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="7ac0b-104">Closes a handle to the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac0b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ac0b-105">Syntax</span></span>


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="7ac0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ac0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ac0b-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ac0b-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ac0b-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="7ac0b-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ac0b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ac0b-109">Return value</span></span>

<span data-ttu-id="7ac0b-110">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7ac0b-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="7ac0b-111">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="7ac0b-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="7ac0b-112">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="7ac0b-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="7ac0b-113">Если указанный ключ является корневым ключом куста реестра, функция завершается с ошибкой \_ Недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="7ac0b-113">If the specified key is the root key of the registry hive, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ac0b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ac0b-114">Remarks</span></span>

<span data-ttu-id="7ac0b-115">Маркер для указанного ключа не должен использоваться после его закрытия, поскольку он больше не будет допустимым.</span><span class="sxs-lookup"><span data-stu-id="7ac0b-115">The handle for a specified key should not be used after it has been closed, because it will no longer be valid.</span></span> <span data-ttu-id="7ac0b-116">Дескрипторы ключей не должны оставаться открытыми больше, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="7ac0b-116">Key handles should not be left open any longer than necessary.</span></span>

<span data-ttu-id="7ac0b-117">Чтобы закрыть автономный куст реестра, используйте функцию [**орклосехиве**](orclosehive.md) .</span><span class="sxs-lookup"><span data-stu-id="7ac0b-117">Use the [**ORCloseHive**](orclosehive.md) function to close an offline registry hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac0b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7ac0b-118">Requirements</span></span>



| <span data-ttu-id="7ac0b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7ac0b-119">Requirement</span></span> | <span data-ttu-id="7ac0b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7ac0b-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac0b-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7ac0b-121">Redistributable</span></span><br/> | <span data-ttu-id="7ac0b-122">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="7ac0b-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="7ac0b-123">Header</span><span class="sxs-lookup"><span data-stu-id="7ac0b-123">Header</span></span><br/>          | <dl> <span data-ttu-id="7ac0b-124"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ac0b-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ac0b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ac0b-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="7ac0b-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ac0b-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ac0b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ac0b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac0b-128">**орклосехиве**</span><span class="sxs-lookup"><span data-stu-id="7ac0b-128">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="7ac0b-129">**оркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="7ac0b-129">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="7ac0b-130">**орделетекэй**</span><span class="sxs-lookup"><span data-stu-id="7ac0b-130">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="7ac0b-131">**оропенкэй**</span><span class="sxs-lookup"><span data-stu-id="7ac0b-131">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
