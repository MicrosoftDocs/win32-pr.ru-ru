---
title: Метод Креатевинстатион класса Win32_TerminalServiceSetting
description: Создает новый стек прослушивателя на основе уникального сочетания имени прослушивателя и сетевого адаптера.
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Креатевинстатион
- Службы удаленных рабочих столов метода Креатевинстатион, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Креатевинстатион
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 112237a00e9e92a2074ee0b95f9964d73f083e43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672516"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="d1086-106">Метод Креатевинстатион \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="d1086-106">CreateWinstation method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="d1086-107">Метод **креатевинстатион** создает новый стек прослушивателя на основе уникального сочетания имени прослушивателя и сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1086-107">The **CreateWinstation** method creates a new listener stack based on the unique combination of listener name and NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1086-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1086-108">Syntax</span></span>


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a><span data-ttu-id="d1086-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1086-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1086-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d1086-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1086-111">Имя прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="d1086-111">Listener name.</span></span>

</dd> <dt>

<span data-ttu-id="d1086-112">*Винстадривернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d1086-112">*WinstaDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1086-113">Имя драйвера винстатион.</span><span class="sxs-lookup"><span data-stu-id="d1086-113">The winstation driver name.</span></span>

</dd> <dt>

<span data-ttu-id="d1086-114">*Ланаид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d1086-114">*LanaId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1086-115">Номер локальной сети (LANA) NetBIOS для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="d1086-115">NetBIOS Local Area Network Adapter (LANA) number for the NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1086-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1086-116">Return value</span></span>

<span data-ttu-id="d1086-117">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="d1086-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d1086-118">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d1086-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1086-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1086-119">Remarks</span></span>

<span data-ttu-id="d1086-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d1086-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d1086-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="d1086-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d1086-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="d1086-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d1086-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d1086-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1086-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d1086-124">Requirements</span></span>



| <span data-ttu-id="d1086-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d1086-125">Requirement</span></span> | <span data-ttu-id="d1086-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d1086-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1086-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1086-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d1086-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1086-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1086-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1086-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d1086-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1086-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1086-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1086-131">Namespace</span></span><br/>                | <span data-ttu-id="d1086-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="d1086-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d1086-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d1086-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1086-134"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1086-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1086-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d1086-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1086-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1086-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1086-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1086-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1086-138">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="d1086-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

