---
title: Метод Сетклиентваллпапер класса Win32_TSEnvironmentSetting
description: Метод Сетклиентваллпапер задает свойство Клиентваллпапер.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетклиентваллпапер
- Службы удаленных рабочих столов метода Сетклиентваллпапер, класс Win32_TSEnvironmentSetting
- Класс Win32_TSEnvironmentSetting службы удаленных рабочих столов, метод Сетклиентваллпапер
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802093"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="f4ae8-106">Метод Сетклиентваллпапер \_ класса Win32 тсенвиронментсеттинг</span><span class="sxs-lookup"><span data-stu-id="f4ae8-106">SetClientWallPaper method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="f4ae8-107">Метод **сетклиентваллпапер** задает свойство **клиентваллпапер** .</span><span class="sxs-lookup"><span data-stu-id="f4ae8-107">The **SetClientWallPaper** method sets the **ClientWallPaper** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ae8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4ae8-108">Syntax</span></span>


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a><span data-ttu-id="f4ae8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4ae8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ae8-110">*Клиентваллпапер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4ae8-110">*ClientWallPaper* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ae8-111">Флаг отключения или включения свойства **клиентваллпапер** , которое указывает, отображается ли на клиенте фоновый рисунок (или фоновый рисунок).</span><span class="sxs-lookup"><span data-stu-id="f4ae8-111">Flag disabling or enabling the **ClientWallPaper** property, which specifies whether the background (or wallpaper) image is displayed on the client.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="f4ae8-112"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="f4ae8-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="f4ae8-113">Фоновое изображение (или фоновый рисунок) не отображается на клиенте.</span><span class="sxs-lookup"><span data-stu-id="f4ae8-113">The background (or wallpaper) image is not displayed on the client.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="f4ae8-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f4ae8-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f4ae8-115">Фоновое изображение (или фоновый рисунок) отображается на клиенте.</span><span class="sxs-lookup"><span data-stu-id="f4ae8-115">The background (or wallpaper) image is displayed on the client.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ae8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4ae8-116">Return value</span></span>

<span data-ttu-id="f4ae8-117">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="f4ae8-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f4ae8-118">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f4ae8-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="f4ae8-119">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="f4ae8-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ae8-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4ae8-120">Remarks</span></span>

<span data-ttu-id="f4ae8-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f4ae8-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f4ae8-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f4ae8-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f4ae8-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f4ae8-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f4ae8-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f4ae8-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ae8-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f4ae8-125">Requirements</span></span>



| <span data-ttu-id="f4ae8-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f4ae8-126">Requirement</span></span> | <span data-ttu-id="f4ae8-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f4ae8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ae8-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4ae8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ae8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4ae8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4ae8-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4ae8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ae8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4ae8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4ae8-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f4ae8-132">Namespace</span></span><br/>                | <span data-ttu-id="f4ae8-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f4ae8-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f4ae8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f4ae8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4ae8-135"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4ae8-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4ae8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f4ae8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4ae8-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4ae8-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ae8-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4ae8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ae8-139">**\_Тсенвиронментсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f4ae8-139">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

