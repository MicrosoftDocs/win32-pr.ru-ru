---
title: Метод Аддпрограм класса Win32_TSVirtualIP (Бдаифаце. h)
description: Добавляет программу в список программ, использующих виртуализацию IP-адресов.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддпрограм
- Службы удаленных рабочих столов метода Аддпрограм, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Аддпрограм
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de573e8d04500917ed44d5a0453005b3aa691bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801726"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="6c219-106">Метод Аддпрограм \_ класса Win32 тсвиртуалип</span><span class="sxs-lookup"><span data-stu-id="6c219-106">AddProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="6c219-107">Добавляет программу в список программ, использующих виртуализацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="6c219-107">Adds a program to the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c219-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c219-108">Syntax</span></span>


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="6c219-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c219-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c219-110">*Програмпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c219-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c219-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="6c219-111">Type: **string**</span></span>

<span data-ttu-id="6c219-112">Путь и имя файла программы, добавляемой в список.</span><span class="sxs-lookup"><span data-stu-id="6c219-112">The path and file name of the program to add to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c219-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c219-113">Return value</span></span>

<span data-ttu-id="6c219-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c219-114">Type: **uint32**</span></span>

<span data-ttu-id="6c219-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="6c219-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6c219-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6c219-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="6c219-117">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6c219-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c219-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6c219-118">Requirements</span></span>



| <span data-ttu-id="6c219-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6c219-119">Requirement</span></span> | <span data-ttu-id="6c219-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6c219-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c219-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c219-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6c219-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6c219-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6c219-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c219-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6c219-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c219-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="6c219-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6c219-125">Namespace</span></span><br/>                | <span data-ttu-id="6c219-126">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="6c219-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6c219-127">Header</span><span class="sxs-lookup"><span data-stu-id="6c219-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c219-128"><dt>Бдаифаце. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c219-128"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c219-129">MOF</span><span class="sxs-lookup"><span data-stu-id="6c219-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c219-130"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c219-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c219-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6c219-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c219-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c219-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c219-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c219-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c219-134">**\_Тсвиртуалип Win32**</span><span class="sxs-lookup"><span data-stu-id="6c219-134">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





