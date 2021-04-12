---
title: Метод SendMessage класса Win32_VirtualDesktopSession
description: Отправка сообщения пользователю через сеанс виртуального рабочего стола.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- Метод SendMessage службы удаленных рабочих столов
- Метод SendMessage службы удаленных рабочих столов, Win32_VirtualDesktopSession класс
- Win32_VirtualDesktopSession службы удаленных рабочих столов класса, метод SendMessage
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415448"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="0014b-106">Метод SendMessage \_ класса Win32 виртуалдесктопсессион</span><span class="sxs-lookup"><span data-stu-id="0014b-106">SendMessage method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="0014b-107">Отправка сообщения пользователю через сеанс виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="0014b-107">Send a message to the user through the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="0014b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0014b-108">Syntax</span></span>


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a><span data-ttu-id="0014b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0014b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0014b-110">*Название* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0014b-110">*Title* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0014b-111">Заголовок сообщений.</span><span class="sxs-lookup"><span data-stu-id="0014b-111">The title of the messge.</span></span>

</dd> <dt>

<span data-ttu-id="0014b-112">*Сообщение об ошибке* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0014b-112">*Message* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0014b-113">Содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="0014b-113">The content of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0014b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0014b-114">Return value</span></span>

<span data-ttu-id="0014b-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="0014b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0014b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0014b-116">Requirements</span></span>



| <span data-ttu-id="0014b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0014b-117">Requirement</span></span> | <span data-ttu-id="0014b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0014b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0014b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0014b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0014b-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0014b-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0014b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0014b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0014b-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0014b-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0014b-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0014b-123">Namespace</span></span><br/>                | <span data-ttu-id="0014b-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="0014b-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0014b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="0014b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0014b-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0014b-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0014b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0014b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0014b-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0014b-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0014b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0014b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0014b-130">**\_Виртуалдесктопсессион Win32**</span><span class="sxs-lookup"><span data-stu-id="0014b-130">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





