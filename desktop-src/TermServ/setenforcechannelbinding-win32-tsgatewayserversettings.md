---
title: Метод Сетенфорцечаннелбиндинг класса Win32_TSGatewayServerSettings
description: Задает свойство Енфорцечаннелбиндинг.
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетенфорцечаннелбиндинг
- Службы удаленных рабочих столов метода Сетенфорцечаннелбиндинг, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетенфорцечаннелбиндинг
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b236341f0fdac31f80f7e7d77aa12a4b22eb9731
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534412"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="579fe-106">Метод Сетенфорцечаннелбиндинг \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="579fe-106">SetEnforceChannelBinding method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="579fe-107">Задает свойство **енфорцечаннелбиндинг** .</span><span class="sxs-lookup"><span data-stu-id="579fe-107">Sets the **EnforceChannelBinding** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="579fe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="579fe-108">Syntax</span></span>


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a><span data-ttu-id="579fe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="579fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579fe-110">*Енфорцечаннелбиндинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="579fe-110">*EnforceChannelBinding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="579fe-111">Указывает новое значение свойства **енфорцечаннелбиндинг** .</span><span class="sxs-lookup"><span data-stu-id="579fe-111">Specifies the new **EnforceChannelBinding** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579fe-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="579fe-112">Return value</span></span>

<span data-ttu-id="579fe-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="579fe-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="579fe-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="579fe-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="579fe-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="579fe-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="579fe-116">Требования</span><span class="sxs-lookup"><span data-stu-id="579fe-116">Requirements</span></span>



| <span data-ttu-id="579fe-117">Требование</span><span class="sxs-lookup"><span data-stu-id="579fe-117">Requirement</span></span> | <span data-ttu-id="579fe-118">Значение</span><span class="sxs-lookup"><span data-stu-id="579fe-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="579fe-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="579fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="579fe-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="579fe-120">None supported</span></span><br/>                                                                |
| <span data-ttu-id="579fe-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="579fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="579fe-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="579fe-122">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="579fe-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="579fe-123">Namespace</span></span><br/>                | <span data-ttu-id="579fe-124">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="579fe-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="579fe-125">MOF</span><span class="sxs-lookup"><span data-stu-id="579fe-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="579fe-126"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="579fe-126"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="579fe-127">DLL</span><span class="sxs-lookup"><span data-stu-id="579fe-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="579fe-128"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="579fe-128"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="579fe-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="579fe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579fe-130">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="579fe-130">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





