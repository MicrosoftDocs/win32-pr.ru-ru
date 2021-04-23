---
title: Структура MPENDOFLIFE_DATA (Мпклиент. h)
description: '\ 0034; Окончание срока жизни \ 0034; данные уведомления.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA структуры устаревшие функции среды Windows
- Функции PMPENDOFLIFE_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136679"
---
# <a name="mpendoflife_data-structure"></a><span data-ttu-id="342a8-105">\_Структура данных мпендофлифе</span><span class="sxs-lookup"><span data-stu-id="342a8-105">MPENDOFLIFE\_DATA structure</span></span>

<span data-ttu-id="342a8-106">Данные уведомления "окончание срока жизни".</span><span class="sxs-lookup"><span data-stu-id="342a8-106">"End of life" notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="342a8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="342a8-107">Syntax</span></span>


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a><span data-ttu-id="342a8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="342a8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="342a8-109">**фтсигнатурикспири**</span><span class="sxs-lookup"><span data-stu-id="342a8-109">**ftSignatureExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="342a8-110">Тип: **fileTime**</span><span class="sxs-lookup"><span data-stu-id="342a8-110">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="342a8-111">Время истечения срока действия подписи.</span><span class="sxs-lookup"><span data-stu-id="342a8-111">Time when the signature expires.</span></span>

</dd> <dt>

<span data-ttu-id="342a8-112">**фтплатформекспири**</span><span class="sxs-lookup"><span data-stu-id="342a8-112">**ftPlatformExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="342a8-113">Тип: **fileTime**</span><span class="sxs-lookup"><span data-stu-id="342a8-113">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="342a8-114">Время истечения срока действия платформы.</span><span class="sxs-lookup"><span data-stu-id="342a8-114">Time when the platform expires.</span></span>

</dd> <dt>

<span data-ttu-id="342a8-115">**фадминконтроллед**</span><span class="sxs-lookup"><span data-stu-id="342a8-115">**fAdminControlled**</span></span>
</dt> <dd>

<span data-ttu-id="342a8-116">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="342a8-116">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="342a8-117">Значение true, если администратор управляет политикой отображения уведомления.</span><span class="sxs-lookup"><span data-stu-id="342a8-117">True if the administrator controlling the policy for showing the notification.</span></span> <span data-ttu-id="342a8-118">Если этот параметр задан, в пользовательском интерфейсе не отображается уведомление конца строки.</span><span class="sxs-lookup"><span data-stu-id="342a8-118">If set, this tells the UI to not show the EOL notification.</span></span>

</dd> <dt>

<span data-ttu-id="342a8-119">**фендофлифеимпендингорпаст**</span><span class="sxs-lookup"><span data-stu-id="342a8-119">**fEndOfLifeImpendingOrPast**</span></span>
</dt> <dd>

<span data-ttu-id="342a8-120">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="342a8-120">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="342a8-121">Значение true, если "окончание срока жизни" находится в состоянии ожидания или в прошлом.</span><span class="sxs-lookup"><span data-stu-id="342a8-121">True if "End of Life" is pending or past.</span></span> <span data-ttu-id="342a8-122">Если задано значение false, Пользовательский интерфейс и клиенты могут очищать все состояния, связанные с конца строки.</span><span class="sxs-lookup"><span data-stu-id="342a8-122">If false, UI and clients can clear any EOL related states.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="342a8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="342a8-123">Requirements</span></span>



| <span data-ttu-id="342a8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="342a8-124">Requirement</span></span> | <span data-ttu-id="342a8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="342a8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="342a8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="342a8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="342a8-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="342a8-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="342a8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="342a8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="342a8-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="342a8-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="342a8-130">Header</span><span class="sxs-lookup"><span data-stu-id="342a8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="342a8-131"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="342a8-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





