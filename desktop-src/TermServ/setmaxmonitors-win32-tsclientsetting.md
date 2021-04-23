---
title: Метод Сетмаксмониторс класса Win32_TSClientSetting
description: Задает свойство Максмониторс.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетмаксмониторс
- Службы удаленных рабочих столов метода Сетмаксмониторс, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетмаксмониторс
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672712"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="b4fa7-106">Метод Сетмаксмониторс \_ класса Win32 тсклиентсеттинг</span><span class="sxs-lookup"><span data-stu-id="b4fa7-106">SetMaxMonitors method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="b4fa7-107">Задает свойство **максмониторс** .</span><span class="sxs-lookup"><span data-stu-id="b4fa7-107">Sets the **MaxMonitors** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fa7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4fa7-108">Syntax</span></span>


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="b4fa7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4fa7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4fa7-110">*Максмониторс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4fa7-110">*MaxMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4fa7-111">Указывает новое максимальное число мониторов, поддерживаемое сервером.</span><span class="sxs-lookup"><span data-stu-id="b4fa7-111">Specifies the new maximum number of monitors supported by the server.</span></span> <span data-ttu-id="b4fa7-112">Минимальное значение равно 1, а максимальное значение — 10.</span><span class="sxs-lookup"><span data-stu-id="b4fa7-112">The minimum value is 1 and the maximum value is 10.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4fa7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4fa7-113">Return value</span></span>

<span data-ttu-id="b4fa7-114">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="b4fa7-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b4fa7-115">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b4fa7-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="b4fa7-116">Метод возвращает ошибку, если параметры соединения пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="b4fa7-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4fa7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b4fa7-117">Requirements</span></span>



| <span data-ttu-id="b4fa7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b4fa7-118">Requirement</span></span> | <span data-ttu-id="b4fa7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b4fa7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fa7-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4fa7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fa7-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b4fa7-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b4fa7-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4fa7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fa7-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4fa7-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b4fa7-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b4fa7-124">Namespace</span></span><br/>                | <span data-ttu-id="b4fa7-125">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b4fa7-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b4fa7-126">MOF</span><span class="sxs-lookup"><span data-stu-id="b4fa7-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4fa7-127"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4fa7-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4fa7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b4fa7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4fa7-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4fa7-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4fa7-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4fa7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4fa7-131">**\_Тсклиентсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="b4fa7-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





