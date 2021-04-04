---
title: IMsRdpClient9 Синксессиондисплайсеттингс, метод
description: Синхронизирует параметры дисплея сеанса.
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Синксессиондисплайсеттингс
- Службы удаленных рабочих столов метода Синксессиондисплайсеттингс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Синксессиондисплайсеттингс
- Службы удаленных рабочих столов метода Синксессиондисплайсеттингс, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Синксессиондисплайсеттингс
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4429f966c00fb608416d541bec229defeca3e5b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988211"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a><span data-ttu-id="82ab2-108">Метод IMsRdpClient9:: Синксессиондисплайсеттингс</span><span class="sxs-lookup"><span data-stu-id="82ab2-108">IMsRdpClient9::SyncSessionDisplaySettings method</span></span>

<span data-ttu-id="82ab2-109">Синхронизирует параметры дисплея сеанса.</span><span class="sxs-lookup"><span data-stu-id="82ab2-109">Synchronizes session display settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ab2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82ab2-110">Syntax</span></span>


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a><span data-ttu-id="82ab2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="82ab2-111">Parameters</span></span>

<span data-ttu-id="82ab2-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="82ab2-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82ab2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82ab2-113">Return value</span></span>

<span data-ttu-id="82ab2-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="82ab2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="82ab2-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="82ab2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ab2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="82ab2-116">Requirements</span></span>



| <span data-ttu-id="82ab2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="82ab2-117">Requirement</span></span> | <span data-ttu-id="82ab2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="82ab2-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ab2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82ab2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="82ab2-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="82ab2-120">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="82ab2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82ab2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="82ab2-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="82ab2-122">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="82ab2-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="82ab2-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="82ab2-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82ab2-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="82ab2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="82ab2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82ab2-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82ab2-126"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="82ab2-127">IID</span><span class="sxs-lookup"><span data-stu-id="82ab2-127">IID</span></span><br/>                      | <span data-ttu-id="82ab2-128">\_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="82ab2-128">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="82ab2-129">\_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="82ab2-129">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="82ab2-130">IID \_ IMsRdpClient9 определен как 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="82ab2-130">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82ab2-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82ab2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ab2-132">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="82ab2-132">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="82ab2-133">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="82ab2-133">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





