---
title: Имсрдпдривеколлектион Дривебиндекс, свойство
description: Извлекает диск по указанному индексу.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дривебиндекс
- Службы удаленных рабочих столов свойства Дривебиндекс, интерфейс Имсрдпдривеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдривеколлектион, свойство Дривебиндекс
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415857"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a><span data-ttu-id="eea41-106">Имсрдпдривеколлектион: свойство Ривебиндекс:D</span><span class="sxs-lookup"><span data-stu-id="eea41-106">IMsRdpDriveCollection::DriveByIndex property</span></span>

<span data-ttu-id="eea41-107">Извлекает диск по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="eea41-107">Retrieves the drive at the specified index.</span></span>

<span data-ttu-id="eea41-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eea41-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea41-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eea41-109">Syntax</span></span>


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="eea41-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="eea41-110">Property value</span></span>

<span data-ttu-id="eea41-111">Указатель интерфейса [**имсрдпдриве**](imsrdpdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="eea41-111">An [**IMsRdpDrive**](imsrdpdrive.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eea41-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="eea41-112">Error codes</span></span>

<span data-ttu-id="eea41-113">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="eea41-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="eea41-114">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="eea41-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea41-115">Требования</span><span class="sxs-lookup"><span data-stu-id="eea41-115">Requirements</span></span>



| <span data-ttu-id="eea41-116">Требование</span><span class="sxs-lookup"><span data-stu-id="eea41-116">Requirement</span></span> | <span data-ttu-id="eea41-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eea41-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eea41-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eea41-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eea41-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eea41-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="eea41-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eea41-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eea41-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eea41-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="eea41-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="eea41-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="eea41-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea41-123"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="eea41-124">DLL</span><span class="sxs-lookup"><span data-stu-id="eea41-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea41-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea41-125"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="eea41-126">IID</span><span class="sxs-lookup"><span data-stu-id="eea41-126">IID</span></span><br/>                      | <span data-ttu-id="eea41-127">IID \_ имсрдпдривеколлектион определен как 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="eea41-127">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eea41-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eea41-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea41-129">**имсрдпдривеколлектион**</span><span class="sxs-lookup"><span data-stu-id="eea41-129">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





