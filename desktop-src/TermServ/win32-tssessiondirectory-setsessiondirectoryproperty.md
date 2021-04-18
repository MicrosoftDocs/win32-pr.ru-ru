---
title: Метод Сетсессиондиректорипроперти класса Win32_TSSessionDirectory
description: Задает свойство Сессиондиректорилокатион или свойство Сессиондиректориклустернаме для класса.
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсессиондиректорипроперти
- Службы удаленных рабочих столов метода Сетсессиондиректорипроперти, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Сетсессиондиректорипроперти
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32357e662ec9b2edb05d75a2814d5215fc9ec7f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490083"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="79212-106">Метод Сетсессиондиректорипроперти \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="79212-106">SetSessionDirectoryProperty method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="79212-107">Задает свойство **сессиондиректорилокатион** или свойство **сессиондиректориклустернаме** для класса.</span><span class="sxs-lookup"><span data-stu-id="79212-107">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="79212-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79212-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="79212-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="79212-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79212-110">*PropertyName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79212-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79212-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="79212-111">Type: **string**</span></span>

<span data-ttu-id="79212-112">Указывает свойство, которое задается методом.</span><span class="sxs-lookup"><span data-stu-id="79212-112">Specifies the property that the method is setting.</span></span>

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span data-ttu-id="79212-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**сессиондиректорилокатион**</span><span class="sxs-lookup"><span data-stu-id="79212-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span></span>


</dt> <dd>

<span data-ttu-id="79212-114">Метод устанавливает свойство **сессиондиректорилокатион** .</span><span class="sxs-lookup"><span data-stu-id="79212-114">The method is setting the **SessionDirectoryLocation** property.</span></span>

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span data-ttu-id="79212-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**сессиондиректориклустернаме**</span><span class="sxs-lookup"><span data-stu-id="79212-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span></span>


</dt> <dd>

<span data-ttu-id="79212-116">Метод устанавливает свойство **сессиондиректориклустернаме** .</span><span class="sxs-lookup"><span data-stu-id="79212-116">The method is setting the **SessionDirectoryClusterName** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="79212-117">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79212-117">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79212-118">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="79212-118">Type: **string**</span></span>

<span data-ttu-id="79212-119">Новое значение для свойства, указанного параметром *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="79212-119">The new value for the property specified by the *PropertyName* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79212-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79212-120">Return value</span></span>

<span data-ttu-id="79212-121">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79212-121">Type: **uint32**</span></span>

<span data-ttu-id="79212-122">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="79212-122">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="79212-123">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="79212-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="79212-124">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="79212-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="79212-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79212-125">Remarks</span></span>

<span data-ttu-id="79212-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="79212-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="79212-127">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="79212-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="79212-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="79212-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="79212-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="79212-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="79212-130">Требования</span><span class="sxs-lookup"><span data-stu-id="79212-130">Requirements</span></span>



| <span data-ttu-id="79212-131">Требование</span><span class="sxs-lookup"><span data-stu-id="79212-131">Requirement</span></span> | <span data-ttu-id="79212-132">Значение</span><span class="sxs-lookup"><span data-stu-id="79212-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79212-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79212-133">Minimum supported client</span></span><br/> | <span data-ttu-id="79212-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="79212-134">None supported</span></span><br/>                                                               |
| <span data-ttu-id="79212-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79212-135">Minimum supported server</span></span><br/> | <span data-ttu-id="79212-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79212-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79212-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="79212-137">Namespace</span></span><br/>                | <span data-ttu-id="79212-138">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="79212-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="79212-139">MOF</span><span class="sxs-lookup"><span data-stu-id="79212-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79212-140"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79212-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="79212-141">DLL</span><span class="sxs-lookup"><span data-stu-id="79212-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79212-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79212-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79212-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79212-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79212-144">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="79212-144">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

