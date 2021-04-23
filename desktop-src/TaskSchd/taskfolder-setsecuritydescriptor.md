---
title: Таскфолдер. Сетсекуритидескриптор, свойство
description: Для сценариев задает дескриптор безопасности для папки.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- планировщик задач свойства Сетсекуритидескриптор
- Планировщик задач свойства Сетсекуритидескриптор, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, свойство Сетсекуритидескриптор
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988422"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a><span data-ttu-id="16d93-106">Таскфолдер. Сетсекуритидескриптор, свойство</span><span class="sxs-lookup"><span data-stu-id="16d93-106">TaskFolder.SetSecurityDescriptor property</span></span>

<span data-ttu-id="16d93-107">Для сценариев задает дескриптор безопасности для папки.</span><span class="sxs-lookup"><span data-stu-id="16d93-107">For scripting, sets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="16d93-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16d93-108">Syntax</span></span>


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a><span data-ttu-id="16d93-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="16d93-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="16d93-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16d93-110">Remarks</span></span>

<span data-ttu-id="16d93-111">Список управления доступом (ACL) можно указать в дескрипторе безопасности для папки задач, чтобы разрешить или запретить определенным пользователям и группам доступ к папке задач.</span><span class="sxs-lookup"><span data-stu-id="16d93-111">You can specify the access control list (ACL) in the security descriptor for a task folder in order to allow or deny certain users and groups access to a task folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="16d93-112">Требования</span><span class="sxs-lookup"><span data-stu-id="16d93-112">Requirements</span></span>



| <span data-ttu-id="16d93-113">Требование</span><span class="sxs-lookup"><span data-stu-id="16d93-113">Requirement</span></span> | <span data-ttu-id="16d93-114">Значение</span><span class="sxs-lookup"><span data-stu-id="16d93-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16d93-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16d93-115">Minimum supported client</span></span><br/> | <span data-ttu-id="16d93-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16d93-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="16d93-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16d93-117">Minimum supported server</span></span><br/> | <span data-ttu-id="16d93-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16d93-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="16d93-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="16d93-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="16d93-120"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="16d93-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="16d93-121">DLL</span><span class="sxs-lookup"><span data-stu-id="16d93-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16d93-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16d93-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16d93-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16d93-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16d93-124">**Регистередтаск. Сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="16d93-124">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="16d93-125">**Таскфолдер. Жетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="16d93-125">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





