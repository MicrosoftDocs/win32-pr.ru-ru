---
title: Метод Сеталловдвм класса Win32_TSClientSetting
description: Задает свойство Алловдвм.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сеталловдвм
- Службы удаленных рабочих столов метода Сеталловдвм, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сеталловдвм
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39441ba3244f206b057ba47c3cb6f765b5e80604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672637"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="6990e-106">Метод Сеталловдвм \_ класса Win32 тсклиентсеттинг</span><span class="sxs-lookup"><span data-stu-id="6990e-106">SetAllowDwm method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="6990e-107">Задает свойство **алловдвм** .</span><span class="sxs-lookup"><span data-stu-id="6990e-107">Sets the **AllowDwm** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6990e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6990e-108">Syntax</span></span>


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a><span data-ttu-id="6990e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6990e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6990e-110">*Алловдвм* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6990e-110">*AllowDwm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6990e-111">Новое значение свойства **алловдвм** .</span><span class="sxs-lookup"><span data-stu-id="6990e-111">The new **AllowDwm** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6990e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6990e-112">Return value</span></span>

<span data-ttu-id="6990e-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="6990e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6990e-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6990e-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="6990e-115">Метод возвращает ошибку, если параметры соединения пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="6990e-115">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="6990e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6990e-116">Requirements</span></span>



| <span data-ttu-id="6990e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6990e-117">Requirement</span></span> | <span data-ttu-id="6990e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6990e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6990e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6990e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6990e-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6990e-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6990e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6990e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6990e-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6990e-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="6990e-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6990e-123">End of client support</span></span><br/>    | <span data-ttu-id="6990e-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6990e-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6990e-125">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="6990e-125">End of server support</span></span><br/>    | <span data-ttu-id="6990e-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6990e-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="6990e-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6990e-127">Namespace</span></span><br/>                | <span data-ttu-id="6990e-128">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="6990e-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6990e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="6990e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6990e-130"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6990e-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6990e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6990e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6990e-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6990e-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6990e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6990e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6990e-134">**\_Тсклиентсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="6990e-134">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





