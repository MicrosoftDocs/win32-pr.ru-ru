---
title: Метод Сетсессиондиректоряктиве класса Win32_TSSessionDirectory
description: Метод Сетсессиондиректоряктиве задает свойство Сессиондиректоряктиве.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсессиондиректоряктиве
- Службы удаленных рабочих столов метода Сетсессиондиректоряктиве, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Сетсессиондиректоряктиве
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca8709028ee90db549c7cdeb053b04dc88b52ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415316"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="6fb3f-106">Метод Сетсессиондиректоряктиве \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="6fb3f-106">SetSessionDirectoryActive method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="6fb3f-107">Метод **сетсессиондиректоряктиве** задает свойство **сессиондиректоряктиве** .</span><span class="sxs-lookup"><span data-stu-id="6fb3f-107">The **SetSessionDirectoryActive** method sets the **SessionDirectoryActive** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb3f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fb3f-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a><span data-ttu-id="6fb3f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fb3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fb3f-110">*Сессиондиректоряктиве* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6fb3f-110">*SessionDirectoryActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb3f-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-111">Type: **uint32**</span></span>

<span data-ttu-id="6fb3f-112">Флаг отключения или включения службы каталогов сеансов.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-112">Flag disabling or enabling the Session Directory service.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="6fb3f-113"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="6fb3f-114">Отключите службу каталогов сеансов.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-114">Disable the Session Directory service.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="6fb3f-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="6fb3f-116">Включите службу каталогов сеансов.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-116">Enable the Session Directory service.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fb3f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fb3f-117">Return value</span></span>

<span data-ttu-id="6fb3f-118">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-118">Type: **uint32**</span></span>

<span data-ttu-id="6fb3f-119">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6fb3f-120">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6fb3f-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="6fb3f-121">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fb3f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6fb3f-122">Remarks</span></span>

<span data-ttu-id="6fb3f-123">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6fb3f-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6fb3f-124">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="6fb3f-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6fb3f-125">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="6fb3f-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6fb3f-126">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6fb3f-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fb3f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6fb3f-127">Requirements</span></span>



| <span data-ttu-id="6fb3f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6fb3f-128">Requirement</span></span> | <span data-ttu-id="6fb3f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6fb3f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb3f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fb3f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb3f-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6fb3f-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6fb3f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fb3f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb3f-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fb3f-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6fb3f-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6fb3f-134">Namespace</span></span><br/>                | <span data-ttu-id="6fb3f-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="6fb3f-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6fb3f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6fb3f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fb3f-137"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fb3f-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fb3f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6fb3f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fb3f-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fb3f-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fb3f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fb3f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb3f-141">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="6fb3f-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

