---
title: Метод Сетпрофилепас класса Win32_TerminalServiceSetting
description: Метод Сетпрофилепас задает свойство filePath для класса.
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетпрофилепас
- Службы удаленных рабочих столов метода Сетпрофилепас, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сетпрофилепас
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 434909471accc191e79c92287ab6e4ac427bf949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415417"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c97fd-106">Метод Сетпрофилепас \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="c97fd-106">SetProfilePath method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c97fd-107">Метод **сетпрофилепас** задает свойство **FilePath** для класса.</span><span class="sxs-lookup"><span data-stu-id="c97fd-107">The **SetProfilePath** method sets the **ProfilePath** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="c97fd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c97fd-108">Syntax</span></span>


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a><span data-ttu-id="c97fd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c97fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c97fd-110">*Путь к пути* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c97fd-110">*ProfilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97fd-111">Новое значение для свойства **FilePath** , которое указывает путь к профилю для компьютера.</span><span class="sxs-lookup"><span data-stu-id="c97fd-111">The new value for the **ProfilePath** property, which specifies the profile path for the computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c97fd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c97fd-112">Return value</span></span>

<span data-ttu-id="c97fd-113">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="c97fd-113">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c97fd-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c97fd-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c97fd-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c97fd-115">Remarks</span></span>

<span data-ttu-id="c97fd-116">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c97fd-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c97fd-117">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="c97fd-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c97fd-118">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c97fd-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c97fd-119">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c97fd-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c97fd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c97fd-120">Requirements</span></span>



| <span data-ttu-id="c97fd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c97fd-121">Requirement</span></span> | <span data-ttu-id="c97fd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c97fd-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c97fd-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c97fd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c97fd-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c97fd-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c97fd-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c97fd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c97fd-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c97fd-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c97fd-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c97fd-127">Namespace</span></span><br/>                | <span data-ttu-id="c97fd-128">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c97fd-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c97fd-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c97fd-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c97fd-130"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c97fd-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c97fd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c97fd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c97fd-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c97fd-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97fd-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c97fd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97fd-134">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="c97fd-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

