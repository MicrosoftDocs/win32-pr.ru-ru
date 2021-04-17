---
title: Метод Сетколордепсполици класса Win32_TSClientSetting
description: Метод Сетколордепсполици задает свойство Колордепсполици для класса.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетколордепсполици
- Службы удаленных рабочих столов метода Сетколордепсполици, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетколордепсполици
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d47280ce303e7eeba401e0eb34c7f7fa5a7bec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415412"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="4abb5-106">Метод Сетколордепсполици \_ класса Win32 тсклиентсеттинг</span><span class="sxs-lookup"><span data-stu-id="4abb5-106">SetColorDepthPolicy method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="4abb5-107">Метод **сетколордепсполици** задает свойство **колордепсполици** для класса.</span><span class="sxs-lookup"><span data-stu-id="4abb5-107">The **SetColorDepthPolicy** method sets the **ColorDepthPolicy** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="4abb5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4abb5-108">Syntax</span></span>


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="4abb5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4abb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4abb5-110">*Колордепсполици* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4abb5-110">*ColorDepthPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abb5-111">Флаг отключения или включения свойства **сетколордепсполици** , которое указывает, следует ли переопределять максимальное значение цвета пользователя.</span><span class="sxs-lookup"><span data-stu-id="4abb5-111">Flag disabling or enabling the **SetColorDepthPolicy** property, which specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="4abb5-112"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="4abb5-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="4abb5-113">Включите свойство.</span><span class="sxs-lookup"><span data-stu-id="4abb5-113">Enable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="4abb5-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="4abb5-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="4abb5-115">Отключите свойство.</span><span class="sxs-lookup"><span data-stu-id="4abb5-115">Disable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4abb5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4abb5-116">Return value</span></span>

<span data-ttu-id="4abb5-117">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="4abb5-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4abb5-118">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4abb5-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="4abb5-119">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="4abb5-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4abb5-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4abb5-120">Remarks</span></span>

<span data-ttu-id="4abb5-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4abb5-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4abb5-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="4abb5-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4abb5-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4abb5-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4abb5-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4abb5-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4abb5-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4abb5-125">Requirements</span></span>



| <span data-ttu-id="4abb5-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4abb5-126">Requirement</span></span> | <span data-ttu-id="4abb5-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4abb5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4abb5-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4abb5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4abb5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4abb5-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4abb5-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4abb5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4abb5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4abb5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4abb5-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4abb5-132">Namespace</span></span><br/>                | <span data-ttu-id="4abb5-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="4abb5-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4abb5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4abb5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4abb5-135"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4abb5-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4abb5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4abb5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4abb5-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4abb5-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4abb5-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4abb5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abb5-139">**\_Тсклиентсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="4abb5-139">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

