---
title: Метод Export класса Win32_TSVm
description: Извлекает сведения мониторинга сеанса виртуальной машины.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода экспорта
- Службы удаленных рабочих столов метода экспорта, класс Win32_TSVm
- Win32_TSVm службы удаленных рабочих столов класса, метод Export
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672549"
---
# <a name="export-method-of-the-win32_tsvm-class"></a><span data-ttu-id="135f1-106">Метод Export \_ класса Win32 тсвм</span><span class="sxs-lookup"><span data-stu-id="135f1-106">Export method of the Win32\_TSVm class</span></span>

<span data-ttu-id="135f1-107">Извлекает сведения мониторинга сеанса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="135f1-107">Retrieves the virtual machine session monitoring information.</span></span>

## <a name="syntax"></a><span data-ttu-id="135f1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="135f1-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a><span data-ttu-id="135f1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="135f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="135f1-110">*Експортфолдерпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="135f1-110">*ExportFolderPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="135f1-111">Путь к каталогу, в который будет экспортирована виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="135f1-111">Path to where the virtual machine will be exported.</span></span>

</dd> <dt>

<span data-ttu-id="135f1-112">*Експортжобобжектпас* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="135f1-112">*ExportJobObjectPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="135f1-113">При успешном выполнении возвращает путь к объекту HyperV Конкретежоб.</span><span class="sxs-lookup"><span data-stu-id="135f1-113">On a success returns the HyperV ConcreteJob object path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="135f1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="135f1-114">Return value</span></span>

<span data-ttu-id="135f1-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="135f1-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="135f1-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="135f1-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="135f1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="135f1-117">Requirements</span></span>



| <span data-ttu-id="135f1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="135f1-118">Requirement</span></span> | <span data-ttu-id="135f1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="135f1-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="135f1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="135f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="135f1-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="135f1-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="135f1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="135f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="135f1-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="135f1-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="135f1-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="135f1-124">Namespace</span></span><br/>                | <span data-ttu-id="135f1-125">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="135f1-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="135f1-126">MOF</span><span class="sxs-lookup"><span data-stu-id="135f1-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="135f1-127"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="135f1-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="135f1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="135f1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="135f1-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="135f1-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="135f1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="135f1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135f1-131">**\_Тсвм Win32**</span><span class="sxs-lookup"><span data-stu-id="135f1-131">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





