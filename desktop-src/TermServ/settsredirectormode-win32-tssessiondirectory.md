---
title: Метод Сеттсредиректормоде класса Win32_TSSessionDirectory
description: Задает значение, указывающее, будет ли сервер действовать в качестве перенаправления службы удаленных рабочих столов.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сеттсредиректормоде
- Службы удаленных рабочих столов метода Сеттсредиректормоде, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Сеттсредиректормоде
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e3195a83a32dca0c8e4a96de211a72a66a8f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892569"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="f08d7-106">Метод Сеттсредиректормоде \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="f08d7-106">SetTSRedirectorMode method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="f08d7-107">Задает значение, указывающее, будет ли сервер действовать в качестве перенаправления службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f08d7-107">Sets the value to indicate whether the server will act as a Remote Desktop Services redirector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f08d7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f08d7-108">Syntax</span></span>


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a><span data-ttu-id="f08d7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f08d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f08d7-110">*Тсредирвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f08d7-110">*TSRedirValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f08d7-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f08d7-111">Type: **uint32**</span></span>

<span data-ttu-id="f08d7-112">Указывает, будет ли сервер использоваться в качестве перенаправления службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f08d7-112">Specifies if the server will act as a Remote Desktop Services redirector.</span></span> <span data-ttu-id="f08d7-113">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f08d7-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="f08d7-114">0</span><span class="sxs-lookup"><span data-stu-id="f08d7-114">0</span></span>
</dt> <dd>

<span data-ttu-id="f08d7-115">Сервер будет работать как Перенаправитель службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f08d7-115">The server will act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="f08d7-116">1</span><span class="sxs-lookup"><span data-stu-id="f08d7-116">1</span></span>
</dt> <dd>

<span data-ttu-id="f08d7-117">Сервер не будет работать в качестве перенаправления службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f08d7-117">The server will not act as a Remote Desktop Services redirector.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f08d7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f08d7-118">Return value</span></span>

<span data-ttu-id="f08d7-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f08d7-119">Type: **uint32**</span></span>

<span data-ttu-id="f08d7-120">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="f08d7-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f08d7-121">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f08d7-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="f08d7-122">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="f08d7-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="f08d7-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f08d7-123">Remarks</span></span>

<span data-ttu-id="f08d7-124">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f08d7-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f08d7-125">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f08d7-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f08d7-126">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f08d7-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f08d7-127">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f08d7-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f08d7-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f08d7-128">Requirements</span></span>



| <span data-ttu-id="f08d7-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f08d7-129">Requirement</span></span> | <span data-ttu-id="f08d7-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f08d7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f08d7-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f08d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f08d7-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f08d7-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f08d7-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f08d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f08d7-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f08d7-134">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f08d7-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f08d7-135">End of client support</span></span><br/>    | <span data-ttu-id="f08d7-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f08d7-136">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f08d7-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f08d7-137">End of server support</span></span><br/>    | <span data-ttu-id="f08d7-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f08d7-138">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f08d7-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f08d7-139">Namespace</span></span><br/>                | <span data-ttu-id="f08d7-140">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f08d7-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f08d7-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f08d7-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f08d7-142"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f08d7-142"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f08d7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f08d7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f08d7-144"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f08d7-144"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f08d7-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f08d7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08d7-146">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="f08d7-146">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

