---
title: Таскфолдер. Жетсекуритидескриптор, свойство
description: Для сценариев возвращает дескриптор безопасности для папки.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- планировщик задач свойства Жетсекуритидескриптор
- Планировщик задач свойства Жетсекуритидескриптор, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, свойство Жетсекуритидескриптор
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682011"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a><span data-ttu-id="4e7f8-106">Таскфолдер. Жетсекуритидескриптор, свойство</span><span class="sxs-lookup"><span data-stu-id="4e7f8-106">TaskFolder.GetSecurityDescriptor property</span></span>

<span data-ttu-id="4e7f8-107">Для сценариев возвращает дескриптор безопасности для папки.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-107">For scripting, gets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e7f8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e7f8-108">Syntax</span></span>


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a><span data-ttu-id="4e7f8-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4e7f8-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="4e7f8-110">Требования</span><span class="sxs-lookup"><span data-stu-id="4e7f8-110">Requirements</span></span>



| <span data-ttu-id="4e7f8-111">Требование</span><span class="sxs-lookup"><span data-stu-id="4e7f8-111">Requirement</span></span> | <span data-ttu-id="4e7f8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4e7f8-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7f8-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e7f8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4e7f8-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e7f8-114">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4e7f8-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e7f8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4e7f8-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e7f8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e7f8-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4e7f8-117">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e7f8-118"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4e7f8-118"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4e7f8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4e7f8-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e7f8-120"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e7f8-120"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e7f8-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e7f8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7f8-122">**Таскфолдер. Сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="4e7f8-122">**TaskFolder.SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="4e7f8-123">**Регистередтаск. Сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="4e7f8-123">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





