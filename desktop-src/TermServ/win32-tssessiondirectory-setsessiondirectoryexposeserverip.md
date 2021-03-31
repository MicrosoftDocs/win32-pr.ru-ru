---
title: Метод Сетсессиондиректорекспосесерверип класса Win32_TSSessionDirectory
description: Задает свойство Сессиондиректорекспосесерверип.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсессиондиректорекспосесерверип
- Службы удаленных рабочих столов метода Сетсессиондиректорекспосесерверип, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Сетсессиондиректорекспосесерверип
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988509"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="a5765-106">Метод Сетсессиондиректорекспосесерверип \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="a5765-106">SetSessionDirectoryExposeServerIP method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="a5765-107">Задает свойство **сессиондиректорекспосесерверип** .</span><span class="sxs-lookup"><span data-stu-id="a5765-107">Sets the **SessionDirectoryExposeServerIP** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5765-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5765-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a><span data-ttu-id="a5765-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5765-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5765-110">*Сессиондиректорекспосесерверип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5765-110">*SessionDirectoryExposeServerIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5765-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5765-111">Type: **uint32**</span></span>

<span data-ttu-id="a5765-112">Флаг отключения или включения свойства **сессиондиректорекспосесерверип** , которое разрешает или запрещает получение IP-адреса для каталога сеанса.</span><span class="sxs-lookup"><span data-stu-id="a5765-112">Flag disabling or enabling the **SessionDirectoryExposeServerIP** property which allows or denies retrieval of the IP address for the session directory.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a5765-113"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="a5765-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a5765-114">Отключите свойство.</span><span class="sxs-lookup"><span data-stu-id="a5765-114">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a5765-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a5765-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a5765-116">Включите свойство.</span><span class="sxs-lookup"><span data-stu-id="a5765-116">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5765-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5765-117">Return value</span></span>

<span data-ttu-id="a5765-118">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5765-118">Type: **uint32**</span></span>

<span data-ttu-id="a5765-119">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="a5765-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a5765-120">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a5765-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a5765-121">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="a5765-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5765-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5765-122">Remarks</span></span>

<span data-ttu-id="a5765-123">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a5765-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a5765-124">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="a5765-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a5765-125">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a5765-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a5765-126">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a5765-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5765-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a5765-127">Requirements</span></span>



| <span data-ttu-id="a5765-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a5765-128">Requirement</span></span> | <span data-ttu-id="a5765-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a5765-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5765-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5765-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a5765-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5765-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a5765-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5765-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a5765-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5765-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5765-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5765-134">Namespace</span></span><br/>                | <span data-ttu-id="a5765-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a5765-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a5765-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a5765-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5765-137"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5765-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5765-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a5765-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5765-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5765-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5765-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5765-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5765-141">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="a5765-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

