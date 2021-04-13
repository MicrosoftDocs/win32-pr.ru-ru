---
title: Метод Селекталлнетворкадаптерс класса Win32_TSNetworkAdapterSetting
description: Метод Селекталлнетворкадаптерс выбирает все сетевые адаптеры.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Селекталлнетворкадаптерс
- Службы удаленных рабочих столов метода Селекталлнетворкадаптерс, класс Win32_TSNetworkAdapterSetting
- Класс Win32_TSNetworkAdapterSetting службы удаленных рабочих столов, метод Селекталлнетворкадаптерс
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f68245c30fbdbf0721d138d1fc0386c779efe111
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340865"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="229e5-106">Метод Селекталлнетворкадаптерс \_ класса Win32 тснетворкадаптерсеттинг</span><span class="sxs-lookup"><span data-stu-id="229e5-106">SelectAllNetworkAdapters method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="229e5-107">Метод **селекталлнетворкадаптерс** выбирает все сетевые адаптеры.</span><span class="sxs-lookup"><span data-stu-id="229e5-107">The **SelectAllNetworkAdapters** method selects all network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="229e5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="229e5-108">Syntax</span></span>


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a><span data-ttu-id="229e5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="229e5-109">Parameters</span></span>

<span data-ttu-id="229e5-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="229e5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="229e5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="229e5-111">Return value</span></span>

<span data-ttu-id="229e5-112">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="229e5-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="229e5-113">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="229e5-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="229e5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="229e5-114">Remarks</span></span>

<span data-ttu-id="229e5-115">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="229e5-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="229e5-116">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="229e5-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="229e5-117">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="229e5-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="229e5-118">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="229e5-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="229e5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="229e5-119">Requirements</span></span>



| <span data-ttu-id="229e5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="229e5-120">Requirement</span></span> | <span data-ttu-id="229e5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="229e5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="229e5-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="229e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="229e5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="229e5-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="229e5-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="229e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="229e5-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="229e5-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="229e5-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="229e5-126">Namespace</span></span><br/>                | <span data-ttu-id="229e5-127">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="229e5-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="229e5-128">MOF</span><span class="sxs-lookup"><span data-stu-id="229e5-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="229e5-129"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="229e5-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="229e5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="229e5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="229e5-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="229e5-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229e5-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="229e5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229e5-133">**\_Тснетворкадаптерсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="229e5-133">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

