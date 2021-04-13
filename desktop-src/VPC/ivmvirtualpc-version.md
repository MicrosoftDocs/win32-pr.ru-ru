---
title: Свойство версии Ивмвиртуалпк (Впккоминтерфацес. h)
description: Извлекает версию данного экземпляра Windows Virtual PC.
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Свойство версии Virtual PC
- Свойство версии Virtual PC, интерфейс Ивмвиртуалпк
- Виртуальный ПК интерфейса Ивмвиртуалпк, свойство Version
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0dc84fd714c50c0a0adb3084603aeea2419d3ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493113"
---
# <a name="ivmvirtualpcversion-property"></a><span data-ttu-id="8e959-106">Свойство Ивмвиртуалпк:: Version</span><span class="sxs-lookup"><span data-stu-id="8e959-106">IVMVirtualPC::Version property</span></span>

<span data-ttu-id="8e959-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8e959-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e959-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e959-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e959-109">Извлекает версию данного экземпляра Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="8e959-109">Retrieves the version of this instance of Windows Virtual PC.</span></span>

<span data-ttu-id="8e959-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8e959-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e959-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e959-111">Syntax</span></span>


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a><span data-ttu-id="8e959-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8e959-112">Property value</span></span>

<span data-ttu-id="8e959-113">Версия.</span><span class="sxs-lookup"><span data-stu-id="8e959-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8e959-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8e959-114">Error codes</span></span>



| <span data-ttu-id="8e959-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="8e959-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="8e959-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8e959-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e959-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e959-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="8e959-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8e959-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="8e959-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="8e959-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="8e959-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8e959-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="8e959-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8e959-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="8e959-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8e959-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="8e959-123"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="8e959-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="8e959-124">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="8e959-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8e959-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e959-125">Remarks</span></span>

<span data-ttu-id="8e959-126">Сведения о версии Windows Virtual PC возвращаются в виде строкового значения в следующем формате: "*v*. *с*. *BBB*. *tee*", где *v* — номер основной версии, *s* — номер дополнительной версии, *BBB* — номера сборки, *t* — это тип сборки (0 = release build), а *ee* — выпуск сервера (SE = Standard Edition, ee = Enterprise Edition).</span><span class="sxs-lookup"><span data-stu-id="8e959-126">The Windows Virtual PC version information is returned as a string value with the following format: "*v*.*s*.*bbb*.*tee*", where *v* is the major version number, *s* is the minor version number, *bbb* is the build number, *t* is the build type (0 = release build), and *ee* is the server edition (SE = Standard Edition, EE = Enterprise Edition).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e959-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8e959-127">Requirements</span></span>



| <span data-ttu-id="8e959-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8e959-128">Requirement</span></span> | <span data-ttu-id="8e959-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8e959-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e959-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e959-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8e959-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e959-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e959-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e959-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8e959-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8e959-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8e959-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8e959-134">End of client support</span></span><br/>    | <span data-ttu-id="8e959-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e959-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8e959-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="8e959-136">Product</span></span><br/>                  | <span data-ttu-id="8e959-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e959-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8e959-138">Header</span><span class="sxs-lookup"><span data-stu-id="8e959-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e959-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e959-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8e959-140">IID</span><span class="sxs-lookup"><span data-stu-id="8e959-140">IID</span></span><br/>                      | <span data-ttu-id="8e959-141">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="8e959-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8e959-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e959-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e959-143">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="8e959-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

