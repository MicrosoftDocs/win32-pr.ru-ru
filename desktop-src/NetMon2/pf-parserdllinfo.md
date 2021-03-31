---
description: Структура PF \_ парсердллинфо определяет средства синтаксического анализа, расположенные в библиотеке DLL средства синтаксического анализа.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: Структура PF_PARSERDLLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998903"
---
# <a name="pf_parserdllinfo-structure"></a><span data-ttu-id="4a4aa-103">\_Структура PF парсердллинфо</span><span class="sxs-lookup"><span data-stu-id="4a4aa-103">PF\_PARSERDLLINFO structure</span></span>

<span data-ttu-id="4a4aa-104">Структура **PF \_ парсердллинфо** определяет средства синтаксического анализа, расположенные в библиотеке DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-104">The **PF\_PARSERDLLINFO** structure defines the parsers located in the parser DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a4aa-105">Syntax</span></span>


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a><span data-ttu-id="4a4aa-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4a4aa-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a4aa-107">**нпарсерс**</span><span class="sxs-lookup"><span data-stu-id="4a4aa-107">**nParsers**</span></span>
</dt> <dd>

<span data-ttu-id="4a4aa-108">Количество синтаксических анализаторов в библиотеке DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-108">Number of parsers in the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="4a4aa-109">**парсеринфо**</span><span class="sxs-lookup"><span data-stu-id="4a4aa-109">**ParserInfo**</span></span>
</dt> <dd>

<span data-ttu-id="4a4aa-110">Массив структур [PF \_ парсеринфо](pf-parserinfo.md) , описывающих каждое средство синтаксического анализа в библиотеке DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-110">Array of [PF\_PARSERINFO](pf-parserinfo.md) structures that describe each parser in the parser DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a4aa-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a4aa-111">Remarks</span></span>

<span data-ttu-id="4a4aa-112">Структура **PF \_ парсердллинфо** возвращается функцией экспорта [парсераутоинсталлинфо](parserautoinstallinfo.md) , реализованной в библиотеке DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-112">The **PF\_PARSERDLLINFO** structure is returned by the [ParserAutoInstallInfo](parserautoinstallinfo.md) export function that is implemented in the parser DLL.</span></span> <span data-ttu-id="4a4aa-113">Функция **парсераутоинсталлинфо** определяет количество синтаксических анализаторов в библиотеке DLL и использует массив структур [ \_ парсеринфо PF](pf-parserinfo.md) для описания каждого средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-113">The **ParserAutoInstallInfo** function identifies the number of parsers in the DLL, and uses an array of [PF\_PARSERINFO](pf-parserinfo.md) structures to describe each parser.</span></span>

<span data-ttu-id="4a4aa-114">Структура PF \_ парсердллинфо должна быть выделена с помощью **хеапаллок**.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-114">The PF\_PARSERDLLINFO structure must be allocated using **HeapAlloc**.</span></span>



| <span data-ttu-id="4a4aa-115">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="4a4aa-115">For information on</span></span>                                               | <span data-ttu-id="4a4aa-116">См.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-116">See</span></span>                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="4a4aa-117">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-117">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="4a4aa-118">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="4a4aa-118">Parsers</span></span>](parsers.md)                                                      |
| <span data-ttu-id="4a4aa-119">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-119">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="4a4aa-120">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="4a4aa-120">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                      |
| <span data-ttu-id="4a4aa-121">Реализация **парсераутоинсталлинфо**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-121">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="4a4aa-122">Реализация Парсераутоисталлинфо</span><span class="sxs-lookup"><span data-stu-id="4a4aa-122">Implementing ParserAutoIstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="4a4aa-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4a4aa-123">Requirements</span></span>



| <span data-ttu-id="4a4aa-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4a4aa-124">Requirement</span></span> | <span data-ttu-id="4a4aa-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4a4aa-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4aa-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a4aa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4a4aa-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4a4aa-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4a4aa-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a4aa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4a4aa-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4a4aa-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4a4aa-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4a4aa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a4aa-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a4aa-131"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a4aa-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a4aa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4aa-133">PF \_ парсеринфо</span><span class="sxs-lookup"><span data-stu-id="4a4aa-133">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="4a4aa-134">парсераутоинсталлинфо</span><span class="sxs-lookup"><span data-stu-id="4a4aa-134">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> </dl>

 

 




