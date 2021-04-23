---
title: Метод Сетмаксиресолутион класса Win32_TSClientSetting
description: Задает свойство Максиресолутион.
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетмаксиресолутион
- Службы удаленных рабочих столов метода Сетмаксиресолутион, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетмаксиресолутион
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672657"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="2c640-106">Метод Сетмаксиресолутион \_ класса Win32 тсклиентсеттинг</span><span class="sxs-lookup"><span data-stu-id="2c640-106">SetMaxYResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="2c640-107">Задает свойство **максиресолутион** .</span><span class="sxs-lookup"><span data-stu-id="2c640-107">Sets the **MaxYResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c640-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c640-108">Syntax</span></span>


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a><span data-ttu-id="2c640-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c640-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c640-110">*Максиресолутион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c640-110">*MaxYResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c640-111">Новое максимальное разрешение по оси Y, поддерживаемое сервером.</span><span class="sxs-lookup"><span data-stu-id="2c640-111">The new maximum Y resolution supported by the server.</span></span> <span data-ttu-id="2c640-112">Минимальное значение — 200, а максимальное значение — 2048.</span><span class="sxs-lookup"><span data-stu-id="2c640-112">The minimum value is 200 and the maximum value is 2048.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c640-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c640-113">Return value</span></span>

<span data-ttu-id="2c640-114">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="2c640-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2c640-115">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2c640-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="2c640-116">Метод возвращает ошибку, если параметры соединения пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="2c640-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c640-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2c640-117">Requirements</span></span>



| <span data-ttu-id="2c640-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2c640-118">Requirement</span></span> | <span data-ttu-id="2c640-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2c640-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c640-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c640-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c640-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2c640-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2c640-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c640-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c640-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2c640-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="2c640-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2c640-124">Namespace</span></span><br/>                | <span data-ttu-id="2c640-125">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="2c640-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2c640-126">MOF</span><span class="sxs-lookup"><span data-stu-id="2c640-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c640-127"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c640-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c640-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2c640-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c640-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c640-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c640-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c640-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c640-131">**\_Тсклиентсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="2c640-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





