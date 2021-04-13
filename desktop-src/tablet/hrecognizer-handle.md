---
description: Обработчик ХРЕКОГНИЗЕР используется для создания контекста распознавателя, получения атрибутов и свойств распознавателя, а также для определения свойств пакетов, необходимых распознавателю для выполнения распознавания.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: ХРЕКОГНИЗЕР (краткий обзор. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343745"
---
# <a name="hrecognizer-handle"></a><span data-ttu-id="62f3b-103">ХРЕКОГНИЗЕР, обработчик</span><span class="sxs-lookup"><span data-stu-id="62f3b-103">HRECOGNIZER Handle</span></span>

<span data-ttu-id="62f3b-104">Обработчик **хрекогнизер** используется для создания контекста распознавателя, получения атрибутов и свойств распознавателя, а также для определения свойств пакетов, необходимых распознавателю для выполнения распознавания.</span><span class="sxs-lookup"><span data-stu-id="62f3b-104">An **HRECOGNIZER** handle is used to create a recognizer context, retrieve the recognizer's attributes and properties, and determine which packet properties the recognizer requires to perform recognition.</span></span>


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a><span data-ttu-id="62f3b-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62f3b-105">Remarks</span></span>

<span data-ttu-id="62f3b-106">Следующие функции используют **хрекогнизер**.</span><span class="sxs-lookup"><span data-stu-id="62f3b-106">The following functions use an **HRECOGNIZER**.</span></span>



| <span data-ttu-id="62f3b-107">Функция</span><span class="sxs-lookup"><span data-stu-id="62f3b-107">Function</span></span>                                                               | <span data-ttu-id="62f3b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="62f3b-108">Description</span></span>                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62f3b-109">**креатерекогнизер**</span><span class="sxs-lookup"><span data-stu-id="62f3b-109">**CreateRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | <span data-ttu-id="62f3b-110">Создает распознаватель.</span><span class="sxs-lookup"><span data-stu-id="62f3b-110">Creates a recognizer.</span></span><br/>                                                                   |
| [<span data-ttu-id="62f3b-111">**дестройрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="62f3b-111">**DestroyRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | <span data-ttu-id="62f3b-112">Уничтожает распознаватель.</span><span class="sxs-lookup"><span data-stu-id="62f3b-112">Destroys a recognizer.</span></span><br/>                                                                  |
| [<span data-ttu-id="62f3b-113">**жетрекоаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="62f3b-113">**GetRecoAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | <span data-ttu-id="62f3b-114">Возвращает атрибуты распознавателя.</span><span class="sxs-lookup"><span data-stu-id="62f3b-114">Returns the attributes of the recognizer.</span></span><br/>                                               |
| [<span data-ttu-id="62f3b-115">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="62f3b-115">**CreateContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | <span data-ttu-id="62f3b-116">Создает контекст распознавателя.</span><span class="sxs-lookup"><span data-stu-id="62f3b-116">Creates a recognizer context.</span></span><br/>                                                           |
| [<span data-ttu-id="62f3b-117">**дестройконтекст**</span><span class="sxs-lookup"><span data-stu-id="62f3b-117">**DestroyContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | <span data-ttu-id="62f3b-118">Уничтожает контекст распознавателя.</span><span class="sxs-lookup"><span data-stu-id="62f3b-118">Destroys a recognizer context.</span></span><br/>                                                          |
| [<span data-ttu-id="62f3b-119">**жеталлрекогнизерс**</span><span class="sxs-lookup"><span data-stu-id="62f3b-119">**GetAllRecognizers**</span></span>](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | <span data-ttu-id="62f3b-120">Получает все Распознаватели.</span><span class="sxs-lookup"><span data-stu-id="62f3b-120">Gets all recognizers.</span></span><br/>                                                                   |
| [<span data-ttu-id="62f3b-121">**жетресултпропертилист**</span><span class="sxs-lookup"><span data-stu-id="62f3b-121">**GetResultPropertyList**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | <span data-ttu-id="62f3b-122">Получает список свойств, которые может вернуть распознаватель для диапазона результатов.</span><span class="sxs-lookup"><span data-stu-id="62f3b-122">Retrieves a list of properties the recognizer can return for a result range.</span></span><br/>            |
| [<span data-ttu-id="62f3b-123">**жетпреферредпаккетдескриптион**</span><span class="sxs-lookup"><span data-stu-id="62f3b-123">**GetPreferredPacketDescription**</span></span>](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | <span data-ttu-id="62f3b-124">Извлекает описание пакета, содержащего свойства пакета, которые использует распознаватель.</span><span class="sxs-lookup"><span data-stu-id="62f3b-124">Retrieves a packet description that contains the packet properties the recognizer uses.</span></span><br/> |
| [<span data-ttu-id="62f3b-125">**жетуникодеранжес**</span><span class="sxs-lookup"><span data-stu-id="62f3b-125">**GetUnicodeRanges**</span></span>](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | <span data-ttu-id="62f3b-126">Извлекает диапазоны точек Юникода, которые поддерживает распознаватель.</span><span class="sxs-lookup"><span data-stu-id="62f3b-126">Retrieves the ranges of Unicode points that the recognizer supports.</span></span><br/>                    |
| [<span data-ttu-id="62f3b-127">**лоадкачедаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="62f3b-127">**LoadCachedAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | <span data-ttu-id="62f3b-128">Загружает кэшированные атрибуты распознавателя.</span><span class="sxs-lookup"><span data-stu-id="62f3b-128">Loads the cached attributes of a recognizer.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="62f3b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="62f3b-129">Requirements</span></span>



| <span data-ttu-id="62f3b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="62f3b-130">Requirement</span></span> | <span data-ttu-id="62f3b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="62f3b-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="62f3b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62f3b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="62f3b-133">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="62f3b-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="62f3b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62f3b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="62f3b-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="62f3b-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="62f3b-136">Header</span><span class="sxs-lookup"><span data-stu-id="62f3b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f3b-137"><dt>Напомню. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f3b-137"><dt>Recapis.h</dt></span></span> </dl> |



 

 




