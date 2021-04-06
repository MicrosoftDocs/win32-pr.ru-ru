---
title: Метод Ивмхарддиск Compact (Впккоминтерфацес. h)
description: Сжимает динамически расширяемый образ виртуального жесткого диска.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Компактный метод Virtual PC
- Компактный метод Virtual PC, интерфейс Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, Compact, метод
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803586"
---
# <a name="ivmharddiskcompact-method"></a><span data-ttu-id="71cf8-106">Метод Ивмхарддиск:: Compact</span><span class="sxs-lookup"><span data-stu-id="71cf8-106">IVMHardDisk::Compact method</span></span>

<span data-ttu-id="71cf8-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="71cf8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="71cf8-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="71cf8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="71cf8-109">Сжимает динамически расширяемый образ виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="71cf8-109">Compacts a dynamically expanding virtual hard disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="71cf8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71cf8-110">Syntax</span></span>


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a><span data-ttu-id="71cf8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="71cf8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71cf8-112">*компакттаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="71cf8-112">*compactTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="71cf8-113">Объект [**ивмтаск**](ivmtask.md) , который используется для отслеживания завершения процесса сжатия.</span><span class="sxs-lookup"><span data-stu-id="71cf8-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion the compaction process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71cf8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71cf8-114">Return value</span></span>

<span data-ttu-id="71cf8-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="71cf8-115">This method can return one of these values.</span></span>



| <span data-ttu-id="71cf8-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="71cf8-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="71cf8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="71cf8-117">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71cf8-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="71cf8-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="71cf8-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="71cf8-119">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="71cf8-120"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="71cf8-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="71cf8-121">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="71cf8-121">An unexpected error has occurred.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="71cf8-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="71cf8-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="71cf8-123">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="71cf8-123">The parameter is **NULL**.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="71cf8-124"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ нарушение общего доступа к ошибкам)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="71cf8-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="71cf8-125">Образ виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , используется.</span><span class="sxs-lookup"><span data-stu-id="71cf8-125">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use.</span></span><br/>                                  |
| <dl> <span data-ttu-id="71cf8-126"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (на \_ диске с ошибкой \_ Full)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="71cf8-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="71cf8-127">На томе узла недостаточно места для создания временного файла, необходимого для сжатия этого образа виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="71cf8-127">The host volume does not have enough space to create a temporary file needed for the compaction of this virtual hard disk image.</span></span><br/>     |
| <dl> <span data-ttu-id="71cf8-128"><dt>**Виртуальная машина \_ \_Приложение E \_ завершает работу \_**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="71cf8-128"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="71cf8-129">Невозможно сжать образ виртуального жесткого диска, так как приложение завершает работу.</span><span class="sxs-lookup"><span data-stu-id="71cf8-129">The virtual hard disk image cannot be compacted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="71cf8-130"><dt>**Виртуальная машина \_ E \_ файл \_ доступен \_ только для чтения**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="71cf8-130"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="71cf8-131">Образ виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , помечен как "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="71cf8-131">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                     |
| <dl> <span data-ttu-id="71cf8-132"><dt>**Виртуальная машина \_ \_Неверный \_ \_ \_ тип**</dt> <dt>0xA004067Bного</dt> образа HD</span><span class="sxs-lookup"><span data-stu-id="71cf8-132"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="71cf8-133">Образ виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , должен быть типом изображения **вмдисктипединамик** .</span><span class="sxs-lookup"><span data-stu-id="71cf8-133">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a **vmDiskTypeDynamic** image type.</span></span><br/> |
| <dl> <span data-ttu-id="71cf8-134"><dt>**Виртуальная машина \_ E \_ Недопустимый \_ \_ файл HD**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="71cf8-134"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="71cf8-135">Возможно, образ виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , не является допустимым образом.</span><span class="sxs-lookup"><span data-stu-id="71cf8-135">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="71cf8-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71cf8-136">Remarks</span></span>

<span data-ttu-id="71cf8-137">Чтобы сжать динамически расширяемый образ жесткого диска, необходимо сначала обнулить его свободное пространство на образе диска.</span><span class="sxs-lookup"><span data-stu-id="71cf8-137">To compact a dynamically expanding hard disk image, free space on the disk image should first be zeroed.</span></span>

## <a name="requirements"></a><span data-ttu-id="71cf8-138">Требования</span><span class="sxs-lookup"><span data-stu-id="71cf8-138">Requirements</span></span>



| <span data-ttu-id="71cf8-139">Требование</span><span class="sxs-lookup"><span data-stu-id="71cf8-139">Requirement</span></span> | <span data-ttu-id="71cf8-140">Значение</span><span class="sxs-lookup"><span data-stu-id="71cf8-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="71cf8-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71cf8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="71cf8-142">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="71cf8-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71cf8-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71cf8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="71cf8-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="71cf8-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="71cf8-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="71cf8-145">End of client support</span></span><br/>    | <span data-ttu-id="71cf8-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71cf8-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="71cf8-147">Продукт</span><span class="sxs-lookup"><span data-stu-id="71cf8-147">Product</span></span><br/>                  | <span data-ttu-id="71cf8-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="71cf8-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="71cf8-149">Header</span><span class="sxs-lookup"><span data-stu-id="71cf8-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="71cf8-150"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="71cf8-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="71cf8-151">IID</span><span class="sxs-lookup"><span data-stu-id="71cf8-151">IID</span></span><br/>                      | <span data-ttu-id="71cf8-152">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="71cf8-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="71cf8-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71cf8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71cf8-154">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="71cf8-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

