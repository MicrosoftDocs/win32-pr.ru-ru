---
title: Метод method класса Win32_TSGetIcon
description: Возвращает содержимое указанного значка.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Метод службы удаленных рабочих столов
- Метод службы удаленных рабочих столов, Win32_TSGetIcon класс
- Класс Win32_TSGetIcon службы удаленных рабочих столов, метод "Icon"
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988282"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a><span data-ttu-id="4d7a5-106">Метод method \_ класса Win32 тсжетикон</span><span class="sxs-lookup"><span data-stu-id="4d7a5-106">GetIcon method of the Win32\_TSGetIcon class</span></span>

<span data-ttu-id="4d7a5-107">Возвращает содержимое указанного значка.</span><span class="sxs-lookup"><span data-stu-id="4d7a5-107">Returns the contents of the specified icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7a5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d7a5-108">Syntax</span></span>


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a><span data-ttu-id="4d7a5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d7a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7a5-110">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d7a5-110">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7a5-111">Указывает путь к файлу, содержащему значок</span><span class="sxs-lookup"><span data-stu-id="4d7a5-111">Specifies the path to the file that contains the icon</span></span>

</dd> <dt>

<span data-ttu-id="4d7a5-112">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d7a5-112">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7a5-113">Задает индекс значка в файле.</span><span class="sxs-lookup"><span data-stu-id="4d7a5-113">Specifies the index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="4d7a5-114">*Иконконтентс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4d7a5-114">*IconContents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7a5-115">При успешном завершении содержит содержимое значка.</span><span class="sxs-lookup"><span data-stu-id="4d7a5-115">On successful completion contains the contents of the icon.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d7a5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4d7a5-116">Requirements</span></span>



| <span data-ttu-id="4d7a5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4d7a5-117">Requirement</span></span> | <span data-ttu-id="4d7a5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4d7a5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7a5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d7a5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d7a5-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4d7a5-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4d7a5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d7a5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d7a5-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d7a5-122">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="4d7a5-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4d7a5-123">Namespace</span></span><br/>                | <span data-ttu-id="4d7a5-124">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="4d7a5-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4d7a5-125">MOF</span><span class="sxs-lookup"><span data-stu-id="4d7a5-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d7a5-126"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d7a5-126"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="4d7a5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4d7a5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d7a5-128"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d7a5-128"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7a5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d7a5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7a5-130">**\_Тсжетикон Win32**</span><span class="sxs-lookup"><span data-stu-id="4d7a5-130">**Win32\_TSGetIcon**</span></span>](win32-tsgeticon.md)
</dt> </dl>

 

 





