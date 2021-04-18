---
title: Метод Пингсессиондиректори класса Win32_TSSessionDirectory
description: Проверяет, доступен ли сервер подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Пингсессиондиректори
- Службы удаленных рабочих столов метода Пингсессиондиректори, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Пингсессиондиректори
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4022a0c34094a19651522c3f8153038c6d9df503
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534427"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="93756-106">Метод Пингсессиондиректори \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="93756-106">PingSessionDirectory method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="93756-107">Проверяет, доступен ли сервер подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="93756-107">Checks whether the Remote Desktop Connection Broker (RD Connection Broker) server is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="93756-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93756-108">Syntax</span></span>


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="93756-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="93756-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93756-110">*Имя сервера* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93756-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93756-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="93756-111">Type: **string**</span></span>

<span data-ttu-id="93756-112">Имя сервера RDCB.</span><span class="sxs-lookup"><span data-stu-id="93756-112">Name of the RD Connection Broker server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93756-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93756-113">Return value</span></span>

<span data-ttu-id="93756-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93756-114">Type: **uint32**</span></span>

<span data-ttu-id="93756-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="93756-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="93756-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="93756-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="93756-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93756-117">Remarks</span></span>

<span data-ttu-id="93756-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="93756-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="93756-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="93756-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="93756-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="93756-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="93756-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="93756-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="93756-122">Требования</span><span class="sxs-lookup"><span data-stu-id="93756-122">Requirements</span></span>



| <span data-ttu-id="93756-123">Требование</span><span class="sxs-lookup"><span data-stu-id="93756-123">Requirement</span></span> | <span data-ttu-id="93756-124">Значение</span><span class="sxs-lookup"><span data-stu-id="93756-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93756-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93756-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93756-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="93756-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="93756-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93756-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93756-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93756-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93756-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93756-129">Namespace</span></span><br/>                | <span data-ttu-id="93756-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="93756-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="93756-131">MOF</span><span class="sxs-lookup"><span data-stu-id="93756-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93756-132"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93756-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="93756-133">DLL</span><span class="sxs-lookup"><span data-stu-id="93756-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93756-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93756-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93756-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93756-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93756-136">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="93756-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

