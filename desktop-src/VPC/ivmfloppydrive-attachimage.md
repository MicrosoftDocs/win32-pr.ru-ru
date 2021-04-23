---
title: Метод Ивмфлоппидриве Аттачимаже (Впккоминтерфацес. h)
description: Подключает образ гибкого носителя на узле к дисководу гибких дисков виртуальной машины.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Метод Аттачимаже Virtual PC
- Метод Аттачимаже Virtual PC, интерфейс Ивмфлоппидриве
- Ивмфлоппидриве интерфейс Virtual PC, метод Аттачимаже
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988506"
---
# <a name="ivmfloppydriveattachimage-method"></a><span data-ttu-id="6727a-106">Метод Ивмфлоппидриве:: Аттачимаже</span><span class="sxs-lookup"><span data-stu-id="6727a-106">IVMFloppyDrive::AttachImage method</span></span>

<span data-ttu-id="6727a-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6727a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6727a-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6727a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6727a-109">Подключает образ гибкого носителя на узле к дисководу гибких дисков виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6727a-109">Attaches a floppy media image on the host to the floppy drive of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6727a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6727a-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a><span data-ttu-id="6727a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="6727a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6727a-112">*медиаимажепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6727a-112">*mediaImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6727a-113">Полный путь к подключенному к гибкому образу носителя.</span><span class="sxs-lookup"><span data-stu-id="6727a-113">The full path to the floppy media image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6727a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6727a-114">Return value</span></span>

<span data-ttu-id="6727a-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="6727a-115">This method can return one of these values.</span></span>



| <span data-ttu-id="6727a-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="6727a-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="6727a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6727a-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6727a-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6727a-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="6727a-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6727a-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6727a-120"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6727a-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="6727a-121">Недопустимый параметр *медиаимажепас* .</span><span class="sxs-lookup"><span data-stu-id="6727a-121">The *mediaImagePath* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="6727a-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="6727a-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="6727a-123">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6727a-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="6727a-124"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (Error \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="6727a-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="6727a-125">Недостаточно памяти для выполнения этого запроса.</span><span class="sxs-lookup"><span data-stu-id="6727a-125">There is not enough memory available to complete this request.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="6727a-126"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="6727a-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="6727a-127">Путь, указанный в параметре *медиаимажепас* , слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="6727a-127">The path specified by the *mediaImagePath* parameter is too long.</span></span> <span data-ttu-id="6727a-128">Длина пути должна быть меньше **максимального \_ пути** (260).</span><span class="sxs-lookup"><span data-stu-id="6727a-128">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="6727a-129"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="6727a-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="6727a-130">Параметр *медиаимажепас* содержит недопустимый символ (один из " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="6727a-130">The *mediaImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="6727a-131"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6727a-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="6727a-132">Параметр *медиаимажепас* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="6727a-132">The *mediaImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="6727a-133">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="6727a-133">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="6727a-134"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6727a-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="6727a-135">Конфигурация этой виртуальной машины недопустима или не найдена.</span><span class="sxs-lookup"><span data-stu-id="6727a-135">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="6727a-136"><dt>**Виртуальная машина \_ \_ \_ \_ Ошибка записи образа E**</dt> <dt>0xA00400650</dt></span><span class="sxs-lookup"><span data-stu-id="6727a-136"><dt>**VM\_E\_IMAGE\_CAPTURE\_FAIL**</dt> <dt>0xA00400650</dt></span></span> </dl>                  | <span data-ttu-id="6727a-137">Не удалось записать указанный файл изображения.</span><span class="sxs-lookup"><span data-stu-id="6727a-137">The image file specified could not be captured.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="6727a-138"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6727a-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="6727a-139">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6727a-139">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="6727a-140">Требования</span><span class="sxs-lookup"><span data-stu-id="6727a-140">Requirements</span></span>



| <span data-ttu-id="6727a-141">Требование</span><span class="sxs-lookup"><span data-stu-id="6727a-141">Requirement</span></span> | <span data-ttu-id="6727a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="6727a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6727a-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6727a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6727a-144">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6727a-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6727a-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6727a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6727a-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6727a-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6727a-147">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6727a-147">End of client support</span></span><br/>    | <span data-ttu-id="6727a-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6727a-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6727a-149">Продукт</span><span class="sxs-lookup"><span data-stu-id="6727a-149">Product</span></span><br/>                  | <span data-ttu-id="6727a-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6727a-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6727a-151">Header</span><span class="sxs-lookup"><span data-stu-id="6727a-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="6727a-152"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="6727a-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6727a-153">IID</span><span class="sxs-lookup"><span data-stu-id="6727a-153">IID</span></span><br/>                      | <span data-ttu-id="6727a-154">IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="6727a-154">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6727a-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6727a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6727a-156">**ивмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="6727a-156">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

