---
title: Метод Ивмфлоппидрививентс Онмедиаинсерт (Впккоминтерфацес. h)
description: Получает уведомление о том, что носитель вставлен в диск. | Метод Ивмфлоппидрививентс Онмедиаинсерт (Впккоминтерфацес. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Метод Онмедиаинсерт Virtual PC
- Метод Онмедиаинсерт Virtual PC, интерфейс Ивмфлоппидрививентс
- Ивмфлоппидрививентс интерфейс Virtual PC, метод Онмедиаинсерт
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694075"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a><span data-ttu-id="5ce10-107">Метод Ивмфлоппидрививентс:: Онмедиаинсерт</span><span class="sxs-lookup"><span data-stu-id="5ce10-107">IVMFloppyDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="5ce10-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5ce10-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5ce10-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5ce10-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5ce10-110">Получает уведомление о том, что носитель вставлен в диск.</span><span class="sxs-lookup"><span data-stu-id="5ce10-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce10-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ce10-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="5ce10-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ce10-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ce10-113">*mediaPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ce10-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce10-114">Буква диска узла или путь к образу дискеты.</span><span class="sxs-lookup"><span data-stu-id="5ce10-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ce10-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ce10-115">Return value</span></span>

<span data-ttu-id="5ce10-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5ce10-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5ce10-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ce10-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ce10-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ce10-118">Remarks</span></span>

<span data-ttu-id="5ce10-119">Этот метод вызывается при вставке носителя (образа гибкого диска или дискеты в дисководе узла).</span><span class="sxs-lookup"><span data-stu-id="5ce10-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is inserted.</span></span> <span data-ttu-id="5ce10-120">Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии вмфлоппидрививент онмедиаинсерт, исходящем от [**ивмфлоппидриве**](ivmfloppydrive.md).</span><span class="sxs-lookup"><span data-stu-id="5ce10-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaInsert event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce10-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5ce10-121">Requirements</span></span>



| <span data-ttu-id="5ce10-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5ce10-122">Requirement</span></span> | <span data-ttu-id="5ce10-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5ce10-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce10-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ce10-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5ce10-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5ce10-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ce10-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ce10-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5ce10-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5ce10-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5ce10-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5ce10-128">End of client support</span></span><br/>    | <span data-ttu-id="5ce10-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ce10-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5ce10-130">Продукт</span><span class="sxs-lookup"><span data-stu-id="5ce10-130">Product</span></span><br/>                  | <span data-ttu-id="5ce10-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5ce10-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5ce10-132">Header</span><span class="sxs-lookup"><span data-stu-id="5ce10-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ce10-133"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ce10-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5ce10-134">IID</span><span class="sxs-lookup"><span data-stu-id="5ce10-134">IID</span></span><br/>                      | <span data-ttu-id="5ce10-135">ДИИД \_ ивмфлоппидрививентс определяется как a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="5ce10-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="5ce10-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ce10-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce10-137">**ивмфлоппидрививентс**</span><span class="sxs-lookup"><span data-stu-id="5ce10-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

