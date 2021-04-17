---
description: Определяет, является ли строка приложения и раздела (&\# 0034; AppName \| топикнаме&\# 0034;) использует правильный синтаксис.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Функция Нддеисвалидапптопиклист (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684299"
---
# <a name="nddeisvalidapptopiclist-function"></a><span data-ttu-id="d5a3a-103">Функция Нддеисвалидапптопиклист</span><span class="sxs-lookup"><span data-stu-id="d5a3a-103">NDdeIsValidAppTopicList function</span></span>

<span data-ttu-id="d5a3a-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d5a3a-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="d5a3a-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="d5a3a-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="d5a3a-106">Определяет, использует ли строка приложения и раздела ("*AppName* \| *топикнаме*") правильный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="d5a3a-106">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a3a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5a3a-107">Syntax</span></span>


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a><span data-ttu-id="d5a3a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5a3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5a3a-109">*таржеттопик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5a3a-109">*targetTopic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5a3a-110">Указатель на строку приложения и раздел для проверки.</span><span class="sxs-lookup"><span data-stu-id="d5a3a-110">A pointer to the application and topic string to validate.</span></span> <span data-ttu-id="d5a3a-111">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d5a3a-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5a3a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5a3a-112">Return value</span></span>

<span data-ttu-id="d5a3a-113">Если параметр *таржеттопик* имеет допустимый синтаксис, возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d5a3a-113">If the *targetTopic* parameter has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="d5a3a-114">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d5a3a-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5a3a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5a3a-115">Remarks</span></span>

<span data-ttu-id="d5a3a-116">Эта функция также вызывается [**нддешареадд**](nddeshareadd.md) при создании общего ресурса DDE.</span><span class="sxs-lookup"><span data-stu-id="d5a3a-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5a3a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d5a3a-117">Requirements</span></span>



| <span data-ttu-id="d5a3a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d5a3a-118">Requirement</span></span> | <span data-ttu-id="d5a3a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d5a3a-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a3a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5a3a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a3a-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d5a3a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d5a3a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5a3a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a3a-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d5a3a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d5a3a-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d5a3a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5a3a-125"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5a3a-125"><dt>Nddeapi.h</dt></span></span> </dl>      |
| <span data-ttu-id="d5a3a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5a3a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5a3a-127"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5a3a-127"><dt>Nddeapi.lib</dt></span></span> </dl>    |
| <span data-ttu-id="d5a3a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d5a3a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5a3a-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5a3a-129"><dt>Nddeapi.dll</dt></span></span> </dl>    |
| <span data-ttu-id="d5a3a-130">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d5a3a-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d5a3a-131">**Нддеисвалидапптопиклиств** (Юникод) и **нддеисвалидапптопиклиста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d5a3a-131">**NDdeIsValidAppTopicListW** (Unicode) and **NDdeIsValidAppTopicListA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5a3a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5a3a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a3a-133">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="d5a3a-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="d5a3a-134">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="d5a3a-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="d5a3a-135">**нддешареадд**</span><span class="sxs-lookup"><span data-stu-id="d5a3a-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




