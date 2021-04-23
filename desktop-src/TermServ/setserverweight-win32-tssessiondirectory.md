---
title: Метод Сетсервервеигхт класса Win32_TSSessionDirectory
description: Задает значение веса сервера для балансировки нагрузки подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсервервеигхт
- Службы удаленных рабочих столов метода Сетсервервеигхт, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Сетсервервеигхт
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491607"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="58c03-106">Метод Сетсервервеигхт \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="58c03-106">SetServerWeight method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="58c03-107">Задает значение веса сервера для балансировки нагрузки подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="58c03-107">Sets the server weight value for Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c03-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58c03-108">Syntax</span></span>


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a><span data-ttu-id="58c03-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="58c03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c03-110">*Сервервеигхтвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="58c03-110">*ServerWeightValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c03-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58c03-111">Type: **uint32**</span></span>

<span data-ttu-id="58c03-112">Значение веса сервера.</span><span class="sxs-lookup"><span data-stu-id="58c03-112">The server weight value.</span></span> <span data-ttu-id="58c03-113">Допустимый диапазон — от 1 до 10000.</span><span class="sxs-lookup"><span data-stu-id="58c03-113">The valid range is 1 to 10000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58c03-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58c03-114">Remarks</span></span>

<span data-ttu-id="58c03-115">По умолчанию в пользовательском интерфейсе службы удаленных рабочих столов конфигурации значение веса сервера равно 100.</span><span class="sxs-lookup"><span data-stu-id="58c03-115">By default in the user interface of Remote Desktop Services Configuration, the server weight value is 100.</span></span> <span data-ttu-id="58c03-116">Вес сервера является относительным.</span><span class="sxs-lookup"><span data-stu-id="58c03-116">The server weight is relative.</span></span> <span data-ttu-id="58c03-117">Таким образом, если присвоить одному серверу значение 100 и одно значение 200, то сервер с относительным весом, равным 200, получит удвоенное число сеансов.</span><span class="sxs-lookup"><span data-stu-id="58c03-117">Therefore, if you assign one server a value of 100, and one a value of 200, the server with a relative weight of 200 will receive twice the number of sessions.</span></span>

<span data-ttu-id="58c03-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="58c03-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="58c03-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="58c03-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="58c03-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="58c03-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="58c03-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="58c03-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="58c03-122">Требования</span><span class="sxs-lookup"><span data-stu-id="58c03-122">Requirements</span></span>



| <span data-ttu-id="58c03-123">Требование</span><span class="sxs-lookup"><span data-stu-id="58c03-123">Requirement</span></span> | <span data-ttu-id="58c03-124">Значение</span><span class="sxs-lookup"><span data-stu-id="58c03-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58c03-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58c03-125">Minimum supported client</span></span><br/> | <span data-ttu-id="58c03-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="58c03-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="58c03-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58c03-127">Minimum supported server</span></span><br/> | <span data-ttu-id="58c03-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58c03-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58c03-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="58c03-129">Namespace</span></span><br/>                | <span data-ttu-id="58c03-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="58c03-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="58c03-131">MOF</span><span class="sxs-lookup"><span data-stu-id="58c03-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58c03-132"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58c03-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="58c03-133">DLL</span><span class="sxs-lookup"><span data-stu-id="58c03-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58c03-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58c03-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58c03-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58c03-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c03-136">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="58c03-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

