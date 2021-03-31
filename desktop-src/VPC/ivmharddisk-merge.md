---
title: Метод Merge (Впккоминтерфацес. h) Ивмхарддиск
description: Слияние разностного виртуального жесткого диска с образом его родительского диска.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Метод слияния Virtual PC
- Метод слияния Virtual PC, интерфейс Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, метод Merge
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988849"
---
# <a name="ivmharddiskmerge-method"></a><span data-ttu-id="b5a12-106">Метод Ивмхарддиск:: Merge</span><span class="sxs-lookup"><span data-stu-id="b5a12-106">IVMHardDisk::Merge method</span></span>

<span data-ttu-id="b5a12-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b5a12-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b5a12-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b5a12-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b5a12-109">Слияние разностного виртуального жесткого диска с образом его родительского диска.</span><span class="sxs-lookup"><span data-stu-id="b5a12-109">Merges a differencing virtual hard disk with its parent disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a12-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5a12-110">Syntax</span></span>


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="b5a12-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5a12-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a12-112">*мержетаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b5a12-112">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a12-113">Объект [**ивмтаск**](ivmtask.md) , который используется для отслеживания завершения процесса слияния.</span><span class="sxs-lookup"><span data-stu-id="b5a12-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a12-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5a12-114">Return value</span></span>

<span data-ttu-id="b5a12-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="b5a12-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b5a12-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b5a12-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="b5a12-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b5a12-117">Description</span></span>                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5a12-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b5a12-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="b5a12-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b5a12-119">The operation was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b5a12-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b5a12-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="b5a12-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5a12-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="b5a12-122"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ нарушение общего доступа к ошибкам)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="b5a12-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="b5a12-123">Образ виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , используется или является родительским для этого образа виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="b5a12-123">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use or the parent of this virtual hard disk image is in use.</span></span> <span data-ttu-id="b5a12-124">Или эти образы жестких дисков могут быть частью сохраненного состояния.</span><span class="sxs-lookup"><span data-stu-id="b5a12-124">Or, these hard disk images could be part of a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="b5a12-125"><dt>**Виртуальная машина \_ \_Неверный \_ \_ \_ тип**</dt> <dt>0xA004067Bного</dt> образа HD</span><span class="sxs-lookup"><span data-stu-id="b5a12-125"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="b5a12-126">Образ виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , должен быть образом разностного диска.</span><span class="sxs-lookup"><span data-stu-id="b5a12-126">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a differencing disk image.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="b5a12-127"><dt>**Виртуальная машина \_ E \_ файл \_ доступен \_ только для чтения**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="b5a12-127"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="b5a12-128">Родительский элемент образа виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , помечен как "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="b5a12-128">The parent of virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="b5a12-129"><dt>**Виртуальная машина \_ \_ \_ Путь к родительскому каталогу E \_ не \_ найден**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="b5a12-129"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="b5a12-130">Родительский элемент виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , не существует.</span><span class="sxs-lookup"><span data-stu-id="b5a12-130">The parent of the virtual hard disk referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not exist.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="b5a12-131"><dt>**Виртуальная машина \_ \_Приложение E \_ завершает работу \_**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="b5a12-131"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="b5a12-132">Не удается выполнить слияние образа виртуального жесткого диска, так как приложение завершает работу.</span><span class="sxs-lookup"><span data-stu-id="b5a12-132">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="b5a12-133"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b5a12-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="b5a12-134">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b5a12-134">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="b5a12-135">Требования</span><span class="sxs-lookup"><span data-stu-id="b5a12-135">Requirements</span></span>



| <span data-ttu-id="b5a12-136">Требование</span><span class="sxs-lookup"><span data-stu-id="b5a12-136">Requirement</span></span> | <span data-ttu-id="b5a12-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b5a12-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a12-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5a12-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a12-139">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b5a12-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5a12-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5a12-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a12-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b5a12-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b5a12-142">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b5a12-142">End of client support</span></span><br/>    | <span data-ttu-id="b5a12-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b5a12-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b5a12-144">Продукт</span><span class="sxs-lookup"><span data-stu-id="b5a12-144">Product</span></span><br/>                  | <span data-ttu-id="b5a12-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b5a12-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b5a12-146">Header</span><span class="sxs-lookup"><span data-stu-id="b5a12-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5a12-147"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5a12-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b5a12-148">IID</span><span class="sxs-lookup"><span data-stu-id="b5a12-148">IID</span></span><br/>                      | <span data-ttu-id="b5a12-149">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="b5a12-149">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b5a12-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5a12-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a12-151">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="b5a12-151">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

