---
title: Метод Жеттсланаидс класса Win32_TerminalServiceSetting
description: Получает идентификаторы и описания локальных сетевых адаптеров NetBIOS (LANA) и описание службы удаленных рабочих столов сетевых адаптеров.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жеттсланаидс
- Службы удаленных рабочих столов метода Жеттсланаидс, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жеттсланаидс
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d2b2357df7e6d7ccc2cb8a774ba34c50cb46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493200"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="da925-106">Метод Жеттсланаидс \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="da925-106">GetTSLanaIds method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="da925-107">Метод **жеттсланаидс** получает идентификаторы и описания локальных сетевых адаптеров NetBIOS (Lana) и описание службы удаленных рабочих столов сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="da925-107">The **GetTSLanaIds** method gets the NetBIOS Local Area Network Adapter (LANA) IDs and descriptions of Remote Desktop Services network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="da925-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da925-108">Syntax</span></span>


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="da925-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="da925-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da925-110">*Ланаидлист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="da925-110">*LanaIdList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da925-111">Массив номеров LANA.</span><span class="sxs-lookup"><span data-stu-id="da925-111">Array of LANA numbers.</span></span>

</dd> <dt>

<span data-ttu-id="da925-112">*Ланаиддескриптионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="da925-112">*LanaIdDescriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da925-113">Массив описаний LANA, соответствующий массиву *ланаидлист* .</span><span class="sxs-lookup"><span data-stu-id="da925-113">Array of LANA descriptions corresponding to the *LanaIdList* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da925-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da925-114">Return value</span></span>

<span data-ttu-id="da925-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="da925-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="da925-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="da925-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="da925-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da925-117">Remarks</span></span>

<span data-ttu-id="da925-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="da925-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="da925-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="da925-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="da925-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="da925-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="da925-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="da925-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="da925-122">Требования</span><span class="sxs-lookup"><span data-stu-id="da925-122">Requirements</span></span>



| <span data-ttu-id="da925-123">Требование</span><span class="sxs-lookup"><span data-stu-id="da925-123">Requirement</span></span> | <span data-ttu-id="da925-124">Значение</span><span class="sxs-lookup"><span data-stu-id="da925-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da925-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da925-125">Minimum supported client</span></span><br/> | <span data-ttu-id="da925-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da925-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da925-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da925-127">Minimum supported server</span></span><br/> | <span data-ttu-id="da925-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da925-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da925-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="da925-129">Namespace</span></span><br/>                | <span data-ttu-id="da925-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="da925-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="da925-131">MOF</span><span class="sxs-lookup"><span data-stu-id="da925-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da925-132"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da925-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="da925-133">DLL</span><span class="sxs-lookup"><span data-stu-id="da925-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da925-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da925-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da925-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da925-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da925-136">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="da925-136">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

