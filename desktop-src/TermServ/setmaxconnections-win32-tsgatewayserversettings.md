---
title: Метод Сетмаксконнектионс класса Win32_TSGatewayServerSettings
description: Задает свойства MaxConnections и Унлимитедконнектионс, которые управляют максимальным числом разрешенных подключений к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетмаксконнектионс
- Службы удаленных рабочих столов метода Сетмаксконнектионс, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетмаксконнектионс
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e8a2fa18491232a058913fd338bb871b0a98aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672749"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="b5062-106">Метод Сетмаксконнектионс \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="b5062-106">SetMaxConnections method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="b5062-107">Задает свойства **MaxConnections** и **унлимитедконнектионс** , которые управляют максимальным числом разрешенных подключений к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="b5062-107">Sets the **MaxConnections** and **UnlimitedConnections** properties, which control the maximum number of allowed connections to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5062-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5062-108">Syntax</span></span>


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a><span data-ttu-id="b5062-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5062-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5062-110">*Подключения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5062-110">*Connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5062-111">Число подключений, которое должен принять этот сервер.</span><span class="sxs-lookup"><span data-stu-id="b5062-111">Number of connections that this server should accept.</span></span> <span data-ttu-id="b5062-112">Для неограниченного числа соединений установите для параметра *Unlimited* значение **true**.</span><span class="sxs-lookup"><span data-stu-id="b5062-112">For an unlimited number of connections, set the *IsUnlimited* parameter to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="b5062-113">*Без ограничений* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5062-113">*IsUnlimited* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5062-114">**Значение true** показывает, что подключения к службе не ограничиваются указанным числом.</span><span class="sxs-lookup"><span data-stu-id="b5062-114">If **True**, connections to the service are not limited to a specific number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5062-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5062-115">Return value</span></span>

<span data-ttu-id="b5062-116">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b5062-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b5062-117">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b5062-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b5062-118">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b5062-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5062-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5062-119">Remarks</span></span>

<span data-ttu-id="b5062-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="b5062-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b5062-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b5062-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b5062-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="b5062-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b5062-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="b5062-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b5062-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b5062-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5062-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b5062-125">Requirements</span></span>



| <span data-ttu-id="b5062-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b5062-126">Requirement</span></span> | <span data-ttu-id="b5062-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b5062-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5062-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5062-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b5062-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b5062-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b5062-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5062-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b5062-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5062-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b5062-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b5062-132">Namespace</span></span><br/>                | <span data-ttu-id="b5062-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b5062-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b5062-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b5062-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5062-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5062-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5062-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b5062-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5062-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5062-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b5062-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5062-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5062-139">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="b5062-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

