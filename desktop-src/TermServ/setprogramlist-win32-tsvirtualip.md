---
title: Метод Сетпрограмлист класса Win32_TSVirtualIP
description: Перезаписывает список программ, использующих виртуализацию IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетпрограмлист
- Службы удаленных рабочих столов метода Сетпрограмлист, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Сетпрограмлист
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534409"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="5586b-106">Метод Сетпрограмлист \_ класса Win32 тсвиртуалип</span><span class="sxs-lookup"><span data-stu-id="5586b-106">SetProgramList method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="5586b-107">Перезаписывает список программ, использующих виртуализацию IP.</span><span class="sxs-lookup"><span data-stu-id="5586b-107">Overwrites the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="5586b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5586b-108">Syntax</span></span>


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a><span data-ttu-id="5586b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5586b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5586b-110">*Програмлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5586b-110">*ProgramList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5586b-111">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5586b-111">Type: **string\[\]**</span></span>

<span data-ttu-id="5586b-112">Массив строк, содержащий путь и имена файлов программ, использующих IP-виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="5586b-112">An array of strings that contain the path and file names of the programs that use IP virtualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5586b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5586b-113">Return value</span></span>

<span data-ttu-id="5586b-114">Тип: **unint32**</span><span class="sxs-lookup"><span data-stu-id="5586b-114">Type: **unint32**</span></span>

<span data-ttu-id="5586b-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="5586b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5586b-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5586b-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="5586b-117">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="5586b-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5586b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5586b-118">Requirements</span></span>



| <span data-ttu-id="5586b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5586b-119">Requirement</span></span> | <span data-ttu-id="5586b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5586b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5586b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5586b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5586b-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5586b-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5586b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5586b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5586b-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5586b-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="5586b-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5586b-125">Namespace</span></span><br/>                | <span data-ttu-id="5586b-126">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="5586b-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5586b-127">MOF</span><span class="sxs-lookup"><span data-stu-id="5586b-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5586b-128"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5586b-128"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5586b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5586b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5586b-130"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5586b-130"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5586b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5586b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5586b-132">**\_Тсвиртуалип Win32**</span><span class="sxs-lookup"><span data-stu-id="5586b-132">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





