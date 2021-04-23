---
title: Свойство Parent Ивмхарддиск (Впккоминтерфацес. h)
description: Родительский объект разностного виртуального жесткого диска.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Виртуальный ПК родительского свойства
- Родительский свойств Virtual PC, интерфейс Ивмхарддиск
- Интерфейс Ивмхарддиск Virtual PC, свойство Parent
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988162"
---
# <a name="ivmharddiskparent-property"></a><span data-ttu-id="48114-106">Ивмхарддиск: свойство почему:P</span><span class="sxs-lookup"><span data-stu-id="48114-106">IVMHardDisk::Parent property</span></span>

<span data-ttu-id="48114-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="48114-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="48114-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="48114-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="48114-109">Извлекает и задает родительский объект разностного виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="48114-109">Retrieves and sets the parent of the differencing virtual hard disk.</span></span>

<span data-ttu-id="48114-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="48114-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="48114-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48114-111">Syntax</span></span>


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a><span data-ttu-id="48114-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="48114-112">Property value</span></span>

<span data-ttu-id="48114-113">Задает объект [**ивмхарддиск**](ivmharddisk.md) , связанный с образом родительского жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="48114-113">Sets the [**IVMHardDisk**](ivmharddisk.md) object associated with the parent hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="48114-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="48114-114">Error codes</span></span>



| <span data-ttu-id="48114-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="48114-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="48114-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48114-116">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48114-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="48114-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="48114-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="48114-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="48114-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="48114-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="48114-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="48114-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="48114-121"><dt>С \_ ЛОЖЬ</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="48114-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="48114-122">Это не разностный жесткий диск, поэтому он не имеет родителя.</span><span class="sxs-lookup"><span data-stu-id="48114-122">This is not a differencing hard disk, so it has no parent.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="48114-123"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="48114-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="48114-124">Системе не удалось найти файл родительского виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="48114-124">The system could not find the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="48114-125"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="48114-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="48114-126">Системе не удалось найти путь к файлу родительского виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="48114-126">The system could not find the path to the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="48114-127"><dt>Виртуальная машина \_ \_Образ E \_ HD \_ Open \_ Fail</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="48114-127"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="48114-128">При попытке открыть текущий файл образа жесткого диска произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="48114-128">An error occurred while attempting to open the current hard disk image file.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="48114-129"><dt>Виртуальная машина \_ 0xA0040681 \_ \_ \_ доступа к образу HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="48114-129"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="48114-130">Произошла ошибка при попытке доступа к текущему файлу образа жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="48114-130">An error occurred while attempting to access the current hard disk image file.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="48114-131"><dt>Виртуальная машина \_ \_Несоответствие \_ \_ идентификатора родительского \_ дочернего элемента E</dt> <dt>0xA0040685</dt></span><span class="sxs-lookup"><span data-stu-id="48114-131"><dt>VM\_E\_PARENT\_CHILD\_ID\_MISMATCH</dt> <dt>0xA0040685</dt></span></span> </dl>            | <span data-ttu-id="48114-132">Образ виртуального жесткого диска, находящийся *родительским* параметром, не имеет того же идентификатора, что и образ дочернего диска.</span><span class="sxs-lookup"><span data-stu-id="48114-132">The virtual hard disk image located by the *parent* parameter does not have the same ID as the child disk image.</span></span> <span data-ttu-id="48114-133">Убедитесь, что родительский образ виртуального жесткого диска, расположенный *родительским* параметром, является тем же образом, который использовался для создания образа разностного виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="48114-133">Make sure the parent virtual hard disk image located by the *parent* parameter is the same image used to create the differencing virtual hard disk image.</span></span><br/> |
| <dl> <span data-ttu-id="48114-134"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="48114-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="48114-135">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="48114-135">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="48114-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48114-136">Remarks</span></span>

<span data-ttu-id="48114-137">Это свойство допустимо только для разностных образов жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="48114-137">This property is only valid with differencing hard disk images.</span></span>

## <a name="requirements"></a><span data-ttu-id="48114-138">Требования</span><span class="sxs-lookup"><span data-stu-id="48114-138">Requirements</span></span>



| <span data-ttu-id="48114-139">Требование</span><span class="sxs-lookup"><span data-stu-id="48114-139">Requirement</span></span> | <span data-ttu-id="48114-140">Значение</span><span class="sxs-lookup"><span data-stu-id="48114-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48114-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48114-141">Minimum supported client</span></span><br/> | <span data-ttu-id="48114-142">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="48114-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="48114-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48114-143">Minimum supported server</span></span><br/> | <span data-ttu-id="48114-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="48114-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="48114-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="48114-145">End of client support</span></span><br/>    | <span data-ttu-id="48114-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="48114-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="48114-147">Продукт</span><span class="sxs-lookup"><span data-stu-id="48114-147">Product</span></span><br/>                  | <span data-ttu-id="48114-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="48114-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="48114-149">Header</span><span class="sxs-lookup"><span data-stu-id="48114-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="48114-150"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="48114-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="48114-151">IID</span><span class="sxs-lookup"><span data-stu-id="48114-151">IID</span></span><br/>                      | <span data-ttu-id="48114-152">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="48114-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="48114-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48114-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48114-154">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="48114-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

