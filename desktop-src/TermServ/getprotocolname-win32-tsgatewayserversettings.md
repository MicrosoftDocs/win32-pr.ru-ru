---
title: Метод Жетпротоколнаме класса Win32_TSGatewayServerSettings
description: Возвращает имя протокола для указанного индекса протокола.
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетпротоколнаме
- Службы удаленных рабочих столов метода Жетпротоколнаме, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Жетпротоколнаме
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81064581b209f047ac492faee6d442b082d038cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136334"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="09352-106">Метод Жетпротоколнаме \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="09352-106">GetProtocolName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="09352-107">Возвращает имя протокола для указанного индекса протокола.</span><span class="sxs-lookup"><span data-stu-id="09352-107">Returns the protocol name for the specified protocol index.</span></span>

## <a name="syntax"></a><span data-ttu-id="09352-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09352-108">Syntax</span></span>


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="09352-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="09352-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09352-110">*Протоколид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09352-110">*ProtocolId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09352-111">Индекс идентификатора протокола.</span><span class="sxs-lookup"><span data-stu-id="09352-111">Index of the protocol identifier.</span></span> <span data-ttu-id="09352-112">Значение должно быть в диапазоне от нуля до значения свойства **макспротоколс** .</span><span class="sxs-lookup"><span data-stu-id="09352-112">The value must be between zero and the value of the **MaxProtocols** property.</span></span>

</dd> <dt>

<span data-ttu-id="09352-113">*ProtocolName* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="09352-113">*ProtocolName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09352-114">Возвращает имя указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="09352-114">Returns the name of the specified protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09352-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09352-115">Return value</span></span>

<span data-ttu-id="09352-116">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="09352-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="09352-117">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="09352-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="09352-118">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="09352-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09352-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09352-119">Remarks</span></span>

<span data-ttu-id="09352-120">Поддерживается один протокол.</span><span class="sxs-lookup"><span data-stu-id="09352-120">One protocol is supported.</span></span>

<span data-ttu-id="09352-121">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="09352-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="09352-122">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="09352-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="09352-123">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="09352-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="09352-124">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="09352-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="09352-125">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="09352-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="09352-126">Требования</span><span class="sxs-lookup"><span data-stu-id="09352-126">Requirements</span></span>



| <span data-ttu-id="09352-127">Требование</span><span class="sxs-lookup"><span data-stu-id="09352-127">Requirement</span></span> | <span data-ttu-id="09352-128">Значение</span><span class="sxs-lookup"><span data-stu-id="09352-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09352-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09352-129">Minimum supported client</span></span><br/> | <span data-ttu-id="09352-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="09352-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="09352-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09352-131">Minimum supported server</span></span><br/> | <span data-ttu-id="09352-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09352-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="09352-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="09352-133">Namespace</span></span><br/>                | <span data-ttu-id="09352-134">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="09352-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="09352-135">MOF</span><span class="sxs-lookup"><span data-stu-id="09352-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09352-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09352-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="09352-137">DLL</span><span class="sxs-lookup"><span data-stu-id="09352-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09352-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09352-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="09352-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09352-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09352-140">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="09352-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

