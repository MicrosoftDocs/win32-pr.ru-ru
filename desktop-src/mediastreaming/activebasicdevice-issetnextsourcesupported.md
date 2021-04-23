---
title: Свойство Иссетнекстсаурцесуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживается ли настройка следующего источника.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- API потоковой передачи мультимедиа свойства Иссетнекстсаурцесуппортед
- API потоковой передачи мультимедиа свойства Иссетнекстсаурцесуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Иссетнекстсаурцесуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710538"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a><span data-ttu-id="6eb2e-106">Свойство Активебасикдевице:: Иссетнекстсаурцесуппортед</span><span class="sxs-lookup"><span data-stu-id="6eb2e-106">ActiveBasicDevice::IsSetNextSourceSupported property</span></span>

<span data-ttu-id="6eb2e-107">Возвращает значение, указывающее, поддерживается ли настройка следующего источника.</span><span class="sxs-lookup"><span data-stu-id="6eb2e-107">Gets a value that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="6eb2e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6eb2e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb2e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6eb2e-109">Syntax</span></span>


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="6eb2e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6eb2e-110">Property value</span></span>

<span data-ttu-id="6eb2e-111">Указатель на **логическое значение** , указывающее, поддерживается ли настройка следующего источника.</span><span class="sxs-lookup"><span data-stu-id="6eb2e-111">A pointer to a **boolean** that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="6eb2e-112">**значение true** , если настройка следующего источника поддерживается; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="6eb2e-112">**true** if setting the next source is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb2e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6eb2e-113">Requirements</span></span>



| <span data-ttu-id="6eb2e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6eb2e-114">Requirement</span></span> | <span data-ttu-id="6eb2e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6eb2e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb2e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6eb2e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6eb2e-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6eb2e-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6eb2e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6eb2e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6eb2e-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6eb2e-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6eb2e-120">Header</span><span class="sxs-lookup"><span data-stu-id="6eb2e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eb2e-121"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb2e-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="6eb2e-122">IDL</span><span class="sxs-lookup"><span data-stu-id="6eb2e-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6eb2e-123"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6eb2e-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="6eb2e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6eb2e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eb2e-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6eb2e-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb2e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6eb2e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6eb2e-127">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6eb2e-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

