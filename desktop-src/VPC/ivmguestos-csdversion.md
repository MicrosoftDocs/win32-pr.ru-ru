---
title: Свойство Ксдверсион Ивмгуестос (Впккоминтерфацес. h)
description: Ксдверсион гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: 6f1d8dd6-6feb-4bdf-a553-631d55c18076
keywords:
- Ксдверсион свойство Virtual PC
- Ксдверсион свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Ксдверсион
topic_type:
- apiref
api_name:
- IVMGuestOS.CSDVersion
- IVMGuestOS.get_CSDVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d82b3939f581edf328902f7fd0a26e1916abe1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989311"
---
# <a name="ivmguestoscsdversion-property"></a><span data-ttu-id="c8608-106">Свойство Ивмгуестос:: Ксдверсион</span><span class="sxs-lookup"><span data-stu-id="c8608-106">IVMGuestOS::CSDVersion property</span></span>

<span data-ttu-id="c8608-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c8608-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8608-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8608-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8608-109">Получает Ксдверсион гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c8608-109">Retrieves the CSDVersion of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="c8608-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c8608-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8608-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8608-111">Syntax</span></span>


```C++
HRESULT get_CSDVersion(
  [out, retval] BSTR *csdVersion
);
```



## <a name="property-value"></a><span data-ttu-id="c8608-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c8608-112">Property value</span></span>

<span data-ttu-id="c8608-113">Строка, завершающаяся нулем, например "пакет обновления 3", которая указывает на последний установленный в системе пакет обновления.</span><span class="sxs-lookup"><span data-stu-id="c8608-113">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="c8608-114">Если пакет обновления не установлен, строка пуста.</span><span class="sxs-lookup"><span data-stu-id="c8608-114">If no Service Pack has been installed, the string is empty.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8608-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c8608-115">Error codes</span></span>



| <span data-ttu-id="c8608-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="c8608-116">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="c8608-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c8608-117">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c8608-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8608-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="c8608-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c8608-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="c8608-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c8608-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="c8608-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c8608-121">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="c8608-122"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="c8608-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="c8608-123">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="c8608-123">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="c8608-124"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="c8608-124"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="c8608-125">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c8608-125">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="c8608-126"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c8608-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="c8608-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c8608-127">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="c8608-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c8608-128">Requirements</span></span>



| <span data-ttu-id="c8608-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c8608-129">Requirement</span></span> | <span data-ttu-id="c8608-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c8608-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8608-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8608-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c8608-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c8608-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8608-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8608-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c8608-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c8608-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c8608-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c8608-135">End of client support</span></span><br/>    | <span data-ttu-id="c8608-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8608-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c8608-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="c8608-137">Product</span></span><br/>                  | <span data-ttu-id="c8608-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8608-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c8608-139">Header</span><span class="sxs-lookup"><span data-stu-id="c8608-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8608-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8608-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c8608-141">IID</span><span class="sxs-lookup"><span data-stu-id="c8608-141">IID</span></span><br/>                      | <span data-ttu-id="c8608-142">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="c8608-142">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c8608-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8608-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8608-144">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="c8608-144">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

