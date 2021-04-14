---
title: Метод Сетмаксксресолутион класса Win32_TSClientSetting
description: Задает свойство Максксресолутион.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетмаксксресолутион
- Службы удаленных рабочих столов метода Сетмаксксресолутион, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетмаксксресолутион
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ab911fd66c7cf6b4f657d8f9e060eccee80675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490305"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="62ba3-106">Метод Сетмаксксресолутион \_ класса Win32 тсклиентсеттинг</span><span class="sxs-lookup"><span data-stu-id="62ba3-106">SetMaxXResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="62ba3-107">Задает свойство **максксресолутион** .</span><span class="sxs-lookup"><span data-stu-id="62ba3-107">Sets the **MaxXResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ba3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62ba3-108">Syntax</span></span>


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a><span data-ttu-id="62ba3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="62ba3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62ba3-110">*Максксресолутион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62ba3-110">*MaxXResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62ba3-111">Новое максимальное разрешение X, поддерживаемое сервером.</span><span class="sxs-lookup"><span data-stu-id="62ba3-111">The new maximum X resolution supported by the server.</span></span> <span data-ttu-id="62ba3-112">Минимальное значение — 200, а максимальное значение — 4096.</span><span class="sxs-lookup"><span data-stu-id="62ba3-112">The minimum value is 200 and maximum value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62ba3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62ba3-113">Return value</span></span>

<span data-ttu-id="62ba3-114">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="62ba3-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="62ba3-115">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="62ba3-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="62ba3-116">Метод возвращает ошибку, если параметры соединения пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="62ba3-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ba3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="62ba3-117">Requirements</span></span>



| <span data-ttu-id="62ba3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="62ba3-118">Requirement</span></span> | <span data-ttu-id="62ba3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="62ba3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62ba3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62ba3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62ba3-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="62ba3-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="62ba3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62ba3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62ba3-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="62ba3-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="62ba3-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62ba3-124">Namespace</span></span><br/>                | <span data-ttu-id="62ba3-125">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="62ba3-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="62ba3-126">MOF</span><span class="sxs-lookup"><span data-stu-id="62ba3-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62ba3-127"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62ba3-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="62ba3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="62ba3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ba3-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ba3-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ba3-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62ba3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ba3-131">**\_Тсклиентсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="62ba3-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





