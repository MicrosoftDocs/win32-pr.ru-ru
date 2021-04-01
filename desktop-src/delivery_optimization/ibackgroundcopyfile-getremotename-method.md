---
title: Метод Ибаккграундкопифиле Жетремотенаме (Deliveryoptimization. h)
description: Извлекает удаленное имя файла.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Метод Жетремотенаме
- Метод Жетремотенаме, интерфейс Ибаккграундкопифиле
- Интерфейс Ибаккграундкопифиле, метод Жетремотенаме
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071537"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a><span data-ttu-id="5b4e0-106">Метод Ибаккграундкопифиле:: Жетремотенаме</span><span class="sxs-lookup"><span data-stu-id="5b4e0-106">IBackgroundCopyFile::GetRemoteName method</span></span>

<span data-ttu-id="5b4e0-107">Извлекает удаленное имя файла.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-107">Retrieves the remote name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b4e0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b4e0-108">Syntax</span></span>


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="5b4e0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b4e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b4e0-110">*ппнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5b4e0-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4e0-111">Строка, заканчивающаяся нулем и содержащая удаленное имя переносимого файла.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-111">Null-terminated string that contains the remote name of the file to transfer.</span></span> <span data-ttu-id="5b4e0-112">Полное имя.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-112">The name is fully qualified.</span></span> <span data-ttu-id="5b4e0-113">Вызовите функцию [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить *ппнаме* по завершении.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b4e0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b4e0-114">Return value</span></span>

<span data-ttu-id="5b4e0-115">Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.</span><span class="sxs-lookup"><span data-stu-id="5b4e0-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b4e0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b4e0-116">Remarks</span></span>

<span data-ttu-id="5b4e0-117">Чтобы изменить имя удаленного файла, вызовите метод [**IBackgroundCopyFile2:: сетремотенаме**](ibackgroundcopyfile2-setremotename-method.md) .</span><span class="sxs-lookup"><span data-stu-id="5b4e0-117">To change the remote file name, call the [**IBackgroundCopyFile2::SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b4e0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5b4e0-118">Requirements</span></span>



| <span data-ttu-id="5b4e0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5b4e0-119">Requirement</span></span> | <span data-ttu-id="5b4e0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5b4e0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4e0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b4e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5b4e0-122">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="5b4e0-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5b4e0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b4e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5b4e0-124">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="5b4e0-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5b4e0-125">Header</span><span class="sxs-lookup"><span data-stu-id="5b4e0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b4e0-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b4e0-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b4e0-127">IDL</span><span class="sxs-lookup"><span data-stu-id="5b4e0-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b4e0-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b4e0-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="5b4e0-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5b4e0-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b4e0-130"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b4e0-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="5b4e0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5b4e0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b4e0-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b4e0-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="5b4e0-133">IID</span><span class="sxs-lookup"><span data-stu-id="5b4e0-133">IID</span></span><br/>                      | <span data-ttu-id="5b4e0-134">IID_IBackgroundCopyFile определен как 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="5b4e0-134">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="5b4e0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b4e0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b4e0-136">**ибаккграундкопифиле**</span><span class="sxs-lookup"><span data-stu-id="5b4e0-136">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="5b4e0-137">**Ибаккграундкопифиле:: Жетлокалнаме**</span><span class="sxs-lookup"><span data-stu-id="5b4e0-137">**IBackgroundCopyFile::GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

