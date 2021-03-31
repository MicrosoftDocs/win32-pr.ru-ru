---
title: Метод Ибаккграундкопифиле Жетлокалнаме (Deliveryoptimization. h)
description: Возвращает локальное имя файла.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- Метод Жетлокалнаме
- Метод Жетлокалнаме, интерфейс Ибаккграундкопифиле
- Интерфейс Ибаккграундкопифиле, метод Жетлокалнаме
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071539"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a><span data-ttu-id="e1d4d-106">Метод Ибаккграундкопифиле:: Жетлокалнаме</span><span class="sxs-lookup"><span data-stu-id="e1d4d-106">IBackgroundCopyFile::GetLocalName method</span></span>

<span data-ttu-id="e1d4d-107">Возвращает локальное имя файла.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-107">Retrieves the local name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d4d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1d4d-108">Syntax</span></span>


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="e1d4d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1d4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d4d-110">*ппнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e1d4d-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d4d-111">Строка, заканчивающаяся нулем и содержащая имя файла на клиенте.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-111">Null-terminated string that contains the name of the file on the client.</span></span> <span data-ttu-id="e1d4d-112">Полное имя.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-112">The name is fully qualified.</span></span> <span data-ttu-id="e1d4d-113">Вызовите функцию [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить *ппнаме* по завершении.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d4d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1d4d-114">Return value</span></span>

<span data-ttu-id="e1d4d-115">Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.</span><span class="sxs-lookup"><span data-stu-id="e1d4d-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d4d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e1d4d-116">Requirements</span></span>



| <span data-ttu-id="e1d4d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e1d4d-117">Requirement</span></span> | <span data-ttu-id="e1d4d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e1d4d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d4d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1d4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e1d4d-120">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e1d4d-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e1d4d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1d4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e1d4d-122">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e1d4d-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e1d4d-123">Header</span><span class="sxs-lookup"><span data-stu-id="e1d4d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1d4d-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1d4d-124"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1d4d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="e1d4d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1d4d-126"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1d4d-126"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e1d4d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e1d4d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1d4d-128"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1d4d-128"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e1d4d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e1d4d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1d4d-130"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1d4d-130"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e1d4d-131">IID</span><span class="sxs-lookup"><span data-stu-id="e1d4d-131">IID</span></span><br/>                      | <span data-ttu-id="e1d4d-132">IID_IBackgroundCopyFile определен как 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="e1d4d-132">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="e1d4d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1d4d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d4d-134">**ибаккграундкопифиле**</span><span class="sxs-lookup"><span data-stu-id="e1d4d-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="e1d4d-135">**Ибаккграундкопифиле:: Жетремотенаме**</span><span class="sxs-lookup"><span data-stu-id="e1d4d-135">**IBackgroundCopyFile::GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

