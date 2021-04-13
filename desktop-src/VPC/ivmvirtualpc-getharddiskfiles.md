---
title: Метод Ивмвиртуалпк Жесарддискфилес (Впккоминтерфацес. h)
description: Извлекает массив известных файлов виртуального жесткого диска.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- Метод Жесарддискфилес Virtual PC
- Метод Жесарддискфилес Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Жесарддискфилес
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4162ae2667d389b445f44973c89a60fafd4c772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535171"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a><span data-ttu-id="a4f37-106">Метод Ивмвиртуалпк:: Жесарддискфилес</span><span class="sxs-lookup"><span data-stu-id="a4f37-106">IVMVirtualPC::GetHardDiskFiles method</span></span>

<span data-ttu-id="a4f37-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a4f37-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a4f37-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a4f37-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a4f37-109">Извлекает массив известных файлов виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="a4f37-109">Retrieves an array of known virtual hard disk files.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f37-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4f37-110">Syntax</span></span>


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a><span data-ttu-id="a4f37-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4f37-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f37-112">*инаддитионалсеарчпасс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4f37-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f37-113">Эти пути будут искаться вместе с путями, заданными в свойстве [**ивмвиртуалпк:: сеарчпасс**](ivmvirtualpc-searchpaths.md) .</span><span class="sxs-lookup"><span data-stu-id="a4f37-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="a4f37-114">*аусарддискфилелист* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a4f37-114">*outHardDiskFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f37-115">Массив строк пути для файлов виртуального жесткого диска, найденных по указанным путям поиска.</span><span class="sxs-lookup"><span data-stu-id="a4f37-115">An array of path strings for the virtual hard disk files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f37-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4f37-116">Return value</span></span>

<span data-ttu-id="a4f37-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a4f37-117">This method can return one of these values.</span></span>



| <span data-ttu-id="a4f37-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="a4f37-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="a4f37-119">Описание</span><span class="sxs-lookup"><span data-stu-id="a4f37-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a4f37-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a4f37-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a4f37-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a4f37-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a4f37-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="a4f37-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a4f37-123">Параметр *аусарддискфилелист* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a4f37-123">The *outHardDiskFileList* parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="a4f37-124"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="a4f37-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="a4f37-125">Параметр *инаддитионалсеарчпасс* не является массивом строк.</span><span class="sxs-lookup"><span data-stu-id="a4f37-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="a4f37-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a4f37-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a4f37-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a4f37-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a4f37-128"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a4f37-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a4f37-129">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="a4f37-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a4f37-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4f37-130">Remarks</span></span>

<span data-ttu-id="a4f37-131">Пути поиска, используемые для получения массива файлов, будут включать наборы, ранее [**ивмвиртуалпк:: сеарчпасс**](ivmvirtualpc-searchpaths.md) , в дополнение к указанным в параметре *инаддитионалсеарчпасс* .</span><span class="sxs-lookup"><span data-stu-id="a4f37-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f37-132">Требования</span><span class="sxs-lookup"><span data-stu-id="a4f37-132">Requirements</span></span>



| <span data-ttu-id="a4f37-133">Требование</span><span class="sxs-lookup"><span data-stu-id="a4f37-133">Requirement</span></span> | <span data-ttu-id="a4f37-134">Значение</span><span class="sxs-lookup"><span data-stu-id="a4f37-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f37-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4f37-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f37-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a4f37-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4f37-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4f37-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f37-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a4f37-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a4f37-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a4f37-139">End of client support</span></span><br/>    | <span data-ttu-id="a4f37-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a4f37-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a4f37-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="a4f37-141">Product</span></span><br/>                  | <span data-ttu-id="a4f37-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a4f37-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a4f37-143">Header</span><span class="sxs-lookup"><span data-stu-id="a4f37-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4f37-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f37-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a4f37-145">IID</span><span class="sxs-lookup"><span data-stu-id="a4f37-145">IID</span></span><br/>                      | <span data-ttu-id="a4f37-146">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a4f37-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a4f37-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4f37-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f37-148">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="a4f37-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

