---
title: Свойство Интегратионкомпонентсверсион Ивмгуестос (Впккоминтерфацес. h)
description: Извлекает версию компонентов интеграции, установленных в гостевой операционной системе.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- Интегратионкомпонентсверсион свойство Virtual PC
- Интегратионкомпонентсверсион свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Интегратионкомпонентсверсион
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85352614b89ab208377fe44fe3b970c693d60dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801276"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a><span data-ttu-id="74d2f-106">Свойство Ивмгуестос:: Интегратионкомпонентсверсион</span><span class="sxs-lookup"><span data-stu-id="74d2f-106">IVMGuestOS::IntegrationComponentsVersion property</span></span>

<span data-ttu-id="74d2f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="74d2f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="74d2f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="74d2f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="74d2f-109">Извлекает версию компонентов интеграции, установленных в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="74d2f-109">Retrieves the version of the Integration Components installed in the guest operating system.</span></span>

<span data-ttu-id="74d2f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="74d2f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="74d2f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74d2f-111">Syntax</span></span>


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a><span data-ttu-id="74d2f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="74d2f-112">Property value</span></span>

<span data-ttu-id="74d2f-113">Версия.</span><span class="sxs-lookup"><span data-stu-id="74d2f-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74d2f-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="74d2f-114">Error codes</span></span>



| <span data-ttu-id="74d2f-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="74d2f-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="74d2f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="74d2f-116">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74d2f-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="74d2f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="74d2f-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="74d2f-118">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="74d2f-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="74d2f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="74d2f-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="74d2f-120">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="74d2f-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="74d2f-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="74d2f-122">Не удалось найти виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="74d2f-122">The virtual machine (VM) could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="74d2f-123"><dt>Виртуальная машина \_ \_ \_ \_ </dt> <dt>Не0xA0040504ные</dt> дополнения</span><span class="sxs-lookup"><span data-stu-id="74d2f-123"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="74d2f-124">Компоненты интеграции не установлены в этой виртуальной машине, или виртуальная машина не была запущена.</span><span class="sxs-lookup"><span data-stu-id="74d2f-124">Integration Components are not installed in this VM, or the VM was never started.</span></span><br/> |
| <dl> <span data-ttu-id="74d2f-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="74d2f-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="74d2f-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="74d2f-126">An unexpected error has occurred.</span></span><br/>                                                 |



## <a name="requirements"></a><span data-ttu-id="74d2f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="74d2f-127">Requirements</span></span>



| <span data-ttu-id="74d2f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="74d2f-128">Requirement</span></span> | <span data-ttu-id="74d2f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="74d2f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d2f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74d2f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="74d2f-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="74d2f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74d2f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74d2f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="74d2f-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74d2f-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="74d2f-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="74d2f-134">End of client support</span></span><br/>    | <span data-ttu-id="74d2f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="74d2f-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="74d2f-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="74d2f-136">Product</span></span><br/>                  | <span data-ttu-id="74d2f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="74d2f-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="74d2f-138">Header</span><span class="sxs-lookup"><span data-stu-id="74d2f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="74d2f-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="74d2f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="74d2f-140">IID</span><span class="sxs-lookup"><span data-stu-id="74d2f-140">IID</span></span><br/>                      | <span data-ttu-id="74d2f-141">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="74d2f-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="74d2f-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74d2f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74d2f-143">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="74d2f-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

