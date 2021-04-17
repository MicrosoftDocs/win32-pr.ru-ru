---
description: Структура PF \_ парсеринфо определяет одно средство синтаксического анализа за раз. В структуре PF \_ парсеринфо средство синтаксического анализа определяется сведениями о протоколе, обнаруженном анализатором.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: Структура PF_PARSERINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674037"
---
# <a name="pf_parserinfo-structure"></a><span data-ttu-id="74feb-104">\_Структура PF парсеринфо</span><span class="sxs-lookup"><span data-stu-id="74feb-104">PF\_PARSERINFO structure</span></span>

<span data-ttu-id="74feb-105">Структура **PF \_ парсеринфо** определяет одно средство синтаксического анализа за раз.</span><span class="sxs-lookup"><span data-stu-id="74feb-105">The **PF\_PARSERINFO** structure defines one parser at a time.</span></span> <span data-ttu-id="74feb-106">В структуре **PF \_ парсеринфо** средство синтаксического анализа определяется сведениями о протоколе, обнаруженном анализатором.</span><span class="sxs-lookup"><span data-stu-id="74feb-106">In the **PF\_PARSERINFO** structure, a parser is defined by the information about the protocol that the parser detects.</span></span>

## <a name="syntax"></a><span data-ttu-id="74feb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74feb-107">Syntax</span></span>


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a><span data-ttu-id="74feb-108">Члены</span><span class="sxs-lookup"><span data-stu-id="74feb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="74feb-109">**сзпротоколнаме**</span><span class="sxs-lookup"><span data-stu-id="74feb-109">**szProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="74feb-110">Имя протокола, обнаруженного анализатором.</span><span class="sxs-lookup"><span data-stu-id="74feb-110">Name of the protocol that the parser detects.</span></span>

</dd> <dt>

<span data-ttu-id="74feb-111">**сзкоммент**</span><span class="sxs-lookup"><span data-stu-id="74feb-111">**szComment**</span></span>
</dt> <dd>

<span data-ttu-id="74feb-112">Краткое описание протокола.</span><span class="sxs-lookup"><span data-stu-id="74feb-112">Brief description of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="74feb-113">**сзелпфиле**</span><span class="sxs-lookup"><span data-stu-id="74feb-113">**szHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="74feb-114">Имя файла справки по протоколу, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="74feb-114">Name of the protocol Help file, if any.</span></span>

</dd> <dt>

<span data-ttu-id="74feb-115">**пвхоканпрецедеме**</span><span class="sxs-lookup"><span data-stu-id="74feb-115">**pWhoCanPrecedeMe**</span></span>
</dt> <dd>

<span data-ttu-id="74feb-116">Указатель на структуру [ \_ следов PF](pf-followset.md) , в которой перечислены протоколы, которые могут предшествовать протоколу, описанному в структуре **PF \_ парсеринфо** .</span><span class="sxs-lookup"><span data-stu-id="74feb-116">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocols that can precede the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="74feb-117">Сетевой монитор добавляет протокол синтаксического анализатора в [*следующий набор*](f.md) всех протоколов в наборе.</span><span class="sxs-lookup"><span data-stu-id="74feb-117">Network Monitor adds the parser protocol to the [*follow set*](f.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="74feb-118">**пвхоканфолловме**</span><span class="sxs-lookup"><span data-stu-id="74feb-118">**pWhoCanFollowMe**</span></span>
</dt> <dd>

<span data-ttu-id="74feb-119">Указатель на структуру [ \_ следов PF](pf-followset.md) , в которой указывается протокол, который может следовать за протоколом, описанным в структуре **PF \_ парсеринфо** .</span><span class="sxs-lookup"><span data-stu-id="74feb-119">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocol that can follow the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="74feb-120">Сетевой монитор добавляет протоколы набора в [*следующий набор*](f.md) протокола средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="74feb-120">Network Monitor adds the protocols of the set to the [*follow set*](f.md) of the parser protocol.</span></span>

</dd> <dt>

<span data-ttu-id="74feb-121">**пвхохандсоффтоме**</span><span class="sxs-lookup"><span data-stu-id="74feb-121">**pWhoHandsOffToMe**</span></span>
</dt> <dd>

<span data-ttu-id="74feb-122">Указатель на структуру [PF \_ хандоффсет](pf-handoffset.md) , которая передает протоколу, описанному структурой **\_ парсеринфо PF** .</span><span class="sxs-lookup"><span data-stu-id="74feb-122">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that hands-off to the protocol that the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="74feb-123">Сетевой монитор добавляет протокол средства синтаксического анализа к переданным [*наборам*](h.md) всех протоколов в наборе.</span><span class="sxs-lookup"><span data-stu-id="74feb-123">Network Monitor adds the parser protocol to the [*handoff sets*](h.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="74feb-124">**пвходоихандоффто**</span><span class="sxs-lookup"><span data-stu-id="74feb-124">**pWhoDoIHandOffTo**</span></span>
</dt> <dd>

<span data-ttu-id="74feb-125">Указатель на структуру [PF \_ хандоффсет](pf-handoffset.md) , в которой перечислены протоколы, к которым передает протокол средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="74feb-125">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that lists the protocols that the parser protocol hands off to.</span></span> <span data-ttu-id="74feb-126">Сетевой монитор добавляет протоколы этого набора в [*набор*](h.md) , переданный протоколом синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="74feb-126">Network Monitor adds the protocols of this set to the [*handoff set*](h.md) of the parser protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74feb-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74feb-127">Remarks</span></span>

<span data-ttu-id="74feb-128">Структура **PF \_ парсеринфо** используется в структуре **PF \_ парсердллинфо** для предоставления описания средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="74feb-128">The **PF\_PARSERINFO** structure is used in the **PF\_PARSERDLLINFO** structure to provide a description of a parser.</span></span> <span data-ttu-id="74feb-129">Сетевой монитор использует описание синтаксического анализатора для обновления файла [*Parser.ini*](p.md) , а также ini-файлы синтаксических анализаторов, которые предшествуют и следуют за протоколом, описанным в структуре **PF \_ парсеринфо** .</span><span class="sxs-lookup"><span data-stu-id="74feb-129">Network Monitor uses the parser description to update the [*Parser.ini*](p.md) file, and the INI files of the parsers that precede and follow the protocol described in the **PF\_PARSERINFO** structure.</span></span>

<span data-ttu-id="74feb-130">Следующий набор задает протоколы, которые следуют за протоколом.</span><span class="sxs-lookup"><span data-stu-id="74feb-130">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="74feb-131">Если анализатор не может определить следующий протокол из данных в экземпляре протокола, сетевой монитор использует следующие наборы.</span><span class="sxs-lookup"><span data-stu-id="74feb-131">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="74feb-132">Следующий набор сохраняется в файле [*Parser.ini*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="74feb-132">A follow set is stored in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="74feb-133">При первом установке средства синтаксического анализа сетевой монитор обновляет следующий набор протоколов синтаксического анализа, перечисленных в **пвхоканпрецедеме** и **пвхоканфолловме**.</span><span class="sxs-lookup"><span data-stu-id="74feb-133">When the parser is installed for the first time, Network Monitor updates the follow set of the parser protocols that are listed in **pWhoCanPrecedeMe** and **pWhoCanFollowMe**.</span></span>

<span data-ttu-id="74feb-134">В переданном наборе указываются протоколы, которые следуют за протоколом.</span><span class="sxs-lookup"><span data-stu-id="74feb-134">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="74feb-135">Средство синтаксического анализа использует переданный набор, только если средство синтаксического анализа может определить следующий протокол из данных в экземпляре протокола.</span><span class="sxs-lookup"><span data-stu-id="74feb-135">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="74feb-136">Переданный набор хранится в INI-файлах каждого средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="74feb-136">A handoff set is stored in the INI files of each parser.</span></span> <span data-ttu-id="74feb-137">При первой установке средства синтаксического анализа сетевой монитор обновляет набираемый набор протоколов синтаксического анализа, перечисленных в **пвхохандсоффтоме** и **пвходоихандоффто**.</span><span class="sxs-lookup"><span data-stu-id="74feb-137">When the parser is installed for the first time, Network Monitor updates the handoff set of the parser protocols that are listed in **pWhoHandsOffToMe** and **pWhoDoIHandOffTo**.</span></span>



| <span data-ttu-id="74feb-138">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="74feb-138">For information on</span></span>                                               | <span data-ttu-id="74feb-139">См.</span><span class="sxs-lookup"><span data-stu-id="74feb-139">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="74feb-140">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="74feb-140">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="74feb-141">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="74feb-141">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="74feb-142">Следующие наборы содержат.</span><span class="sxs-lookup"><span data-stu-id="74feb-142">What follow sets contain.</span></span>                                        | [<span data-ttu-id="74feb-143">Указание набора следования</span><span class="sxs-lookup"><span data-stu-id="74feb-143">Specifying a Follow Set</span></span>](specifying-a-follow-set.md)                       |
| <span data-ttu-id="74feb-144">Какие наборы данных содержат.</span><span class="sxs-lookup"><span data-stu-id="74feb-144">What handoff sets contain.</span></span>                                       | [<span data-ttu-id="74feb-145">Указание переданного набора</span><span class="sxs-lookup"><span data-stu-id="74feb-145">Specifying a Handoff Set</span></span>](specifying-a-handoff-set.md)                     |
| <span data-ttu-id="74feb-146">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="74feb-146">What entry points are included in the parser DLL.</span></span>                | [<span data-ttu-id="74feb-147">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="74feb-147">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="74feb-148">Реализация **парсераутоинсталлинфо**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="74feb-148">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="74feb-149">Реализация Парсераутоинсталлинфо</span><span class="sxs-lookup"><span data-stu-id="74feb-149">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="74feb-150">Требования</span><span class="sxs-lookup"><span data-stu-id="74feb-150">Requirements</span></span>



| <span data-ttu-id="74feb-151">Требование</span><span class="sxs-lookup"><span data-stu-id="74feb-151">Requirement</span></span> | <span data-ttu-id="74feb-152">Значение</span><span class="sxs-lookup"><span data-stu-id="74feb-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74feb-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74feb-153">Minimum supported client</span></span><br/> | <span data-ttu-id="74feb-154">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74feb-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="74feb-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74feb-155">Minimum supported server</span></span><br/> | <span data-ttu-id="74feb-156">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74feb-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74feb-157">Заголовок</span><span class="sxs-lookup"><span data-stu-id="74feb-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="74feb-158"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="74feb-158"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74feb-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74feb-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74feb-160">парсераутоинсталлинфо</span><span class="sxs-lookup"><span data-stu-id="74feb-160">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> <dt>

[<span data-ttu-id="74feb-161">\_следующий PF</span><span class="sxs-lookup"><span data-stu-id="74feb-161">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> <dt>

[<span data-ttu-id="74feb-162">PF \_ хандоффсет</span><span class="sxs-lookup"><span data-stu-id="74feb-162">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> <dt>

[<span data-ttu-id="74feb-163">PF \_ парсердллинфо</span><span class="sxs-lookup"><span data-stu-id="74feb-163">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




