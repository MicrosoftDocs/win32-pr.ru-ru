---
title: Регистередтаск. Жетсекуритидескриптор, метод
description: Для создания скриптов возвращает дескриптор безопасности, который используется в качестве учетных данных для зарегистрированной задачи.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- планировщик задач метода Жетсекуритидескриптор
- Планировщик задач метода Жетсекуритидескриптор, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, метод Жетсекуритидескриптор
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989115"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a><span data-ttu-id="14ef9-106">Регистередтаск. Жетсекуритидескриптор, метод</span><span class="sxs-lookup"><span data-stu-id="14ef9-106">RegisteredTask.GetSecurityDescriptor method</span></span>

<span data-ttu-id="14ef9-107">Для создания скриптов возвращает дескриптор безопасности, который используется в качестве учетных данных для зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="14ef9-107">For scripting, gets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ef9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14ef9-108">Syntax</span></span>


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a><span data-ttu-id="14ef9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="14ef9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14ef9-110">*секуритинформатион*</span><span class="sxs-lookup"><span data-stu-id="14ef9-110">*securityInformation*</span></span> 
</dt> <dd>

<span data-ttu-id="14ef9-111">Сведения о безопасности из [**\_ сведений о безопасности**](/windows/desktop/SecAuthZ/security-information).</span><span class="sxs-lookup"><span data-stu-id="14ef9-111">The security information from [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14ef9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14ef9-112">Return value</span></span>

<span data-ttu-id="14ef9-113">Дескриптор безопасности для зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="14ef9-113">The security descriptor for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="14ef9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="14ef9-114">Requirements</span></span>



| <span data-ttu-id="14ef9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="14ef9-115">Requirement</span></span> | <span data-ttu-id="14ef9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="14ef9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14ef9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14ef9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14ef9-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14ef9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="14ef9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14ef9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14ef9-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14ef9-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14ef9-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="14ef9-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="14ef9-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="14ef9-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="14ef9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="14ef9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14ef9-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14ef9-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ef9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14ef9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ef9-126">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="14ef9-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="14ef9-127">**Таскфолдер. Жетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="14ef9-127">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="14ef9-128">**Регистередтаск. Сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="14ef9-128">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

