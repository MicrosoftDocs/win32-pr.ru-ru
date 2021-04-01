---
title: Метод Ивмвиртуалпк Жетфлоппидискфилес (Впккоминтерфацес. h)
description: Извлекает массив известных файлов виртуальных дискет.
ms.assetid: c40f2780-eb84-4e0c-a493-1d1e5706cc8b
keywords:
- Метод Жетфлоппидискфилес Virtual PC
- Метод Жетфлоппидискфилес Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Жетфлоппидискфилес
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9759a3b909bb4f4ac179c166635185a701a8a16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803731"
---
# <a name="ivmvirtualpcgetfloppydiskfiles-method"></a><span data-ttu-id="d45ba-106">Метод Ивмвиртуалпк:: Жетфлоппидискфилес</span><span class="sxs-lookup"><span data-stu-id="d45ba-106">IVMVirtualPC::GetFloppyDiskFiles method</span></span>

<span data-ttu-id="d45ba-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d45ba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d45ba-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d45ba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d45ba-109">Извлекает массив известных файлов виртуальных дискет.</span><span class="sxs-lookup"><span data-stu-id="d45ba-109">Retrieves an array of known virtual floppy disk files.</span></span>

## <a name="syntax"></a><span data-ttu-id="d45ba-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d45ba-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outFloppyDiskFileList
);
```



## <a name="parameters"></a><span data-ttu-id="d45ba-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d45ba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d45ba-112">*инаддитионалсеарчпасс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d45ba-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d45ba-113">Эти пути будут искаться вместе с путями, заданными в свойстве [**ивмвиртуалпк:: сеарчпасс**](ivmvirtualpc-searchpaths.md) .</span><span class="sxs-lookup"><span data-stu-id="d45ba-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="d45ba-114">*аутфлоппидискфилелист* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d45ba-114">*outFloppyDiskFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d45ba-115">Массив файлов виртуальных гибких дисков, найденных по указанным путям поиска.</span><span class="sxs-lookup"><span data-stu-id="d45ba-115">An array of virtual floppy disk files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d45ba-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d45ba-116">Return value</span></span>

<span data-ttu-id="d45ba-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d45ba-117">This method can return one of these values.</span></span>



| <span data-ttu-id="d45ba-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d45ba-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="d45ba-119">Описание</span><span class="sxs-lookup"><span data-stu-id="d45ba-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d45ba-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d45ba-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="d45ba-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d45ba-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d45ba-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d45ba-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="d45ba-123">Параметр *аутфлоппидискфилелист* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d45ba-123">The *outFloppyDiskFileList* parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d45ba-124"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d45ba-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="d45ba-125">Параметр *инаддитионалсеарчпасс* не является массивом строк.</span><span class="sxs-lookup"><span data-stu-id="d45ba-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="d45ba-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d45ba-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="d45ba-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d45ba-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="d45ba-128"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="d45ba-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="d45ba-129">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="d45ba-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d45ba-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d45ba-130">Remarks</span></span>

<span data-ttu-id="d45ba-131">Пути поиска, используемые для получения массива файлов, будут включать наборы, ранее [**ивмвиртуалпк:: сеарчпасс**](ivmvirtualpc-searchpaths.md) , в дополнение к указанным в параметре *инаддитионалсеарчпасс* и расположении установщика для модуля Integration Components.</span><span class="sxs-lookup"><span data-stu-id="d45ba-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter and the installer location for the integration components module.</span></span>

## <a name="requirements"></a><span data-ttu-id="d45ba-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d45ba-132">Requirements</span></span>



| <span data-ttu-id="d45ba-133">Требование</span><span class="sxs-lookup"><span data-stu-id="d45ba-133">Requirement</span></span> | <span data-ttu-id="d45ba-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d45ba-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d45ba-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d45ba-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d45ba-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d45ba-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d45ba-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d45ba-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d45ba-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d45ba-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d45ba-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d45ba-139">End of client support</span></span><br/>    | <span data-ttu-id="d45ba-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d45ba-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d45ba-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="d45ba-141">Product</span></span><br/>                  | <span data-ttu-id="d45ba-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d45ba-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d45ba-143">Header</span><span class="sxs-lookup"><span data-stu-id="d45ba-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d45ba-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d45ba-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d45ba-145">IID</span><span class="sxs-lookup"><span data-stu-id="d45ba-145">IID</span></span><br/>                      | <span data-ttu-id="d45ba-146">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="d45ba-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d45ba-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d45ba-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d45ba-148">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="d45ba-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

