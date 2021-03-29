---
description: Сетевой монитор использует функцию экспорта Парсераутоинсталлинфо для установки средства синтаксического анализа. При вызове Парсераутоинсталлинфо средство синтаксического анализа возвращает структуру PF \_ парсердллинфо, содержащую всю информацию, которую сетевой монитор требуется для установки библиотеки DLL средства синтаксического анализа.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Реализация Парсераутоинсталлинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d79a9ba5036673acb076be9f3634dae7556b5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674206"
---
# <a name="implementing-parserautoinstallinfo"></a><span data-ttu-id="ff466-104">Реализация Парсераутоинсталлинфо</span><span class="sxs-lookup"><span data-stu-id="ff466-104">Implementing ParserAutoInstallInfo</span></span>

<span data-ttu-id="ff466-105">Сетевой монитор использует функцию экспорта [**парсераутоинсталлинфо**](parserautoinstallinfo.md) для установки средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="ff466-105">Network Monitor uses the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) export function to install a parser.</span></span> <span data-ttu-id="ff466-106">При вызове **парсераутоинсталлинфо** средство синтаксического анализа возвращает структуру [**PF \_ парсердллинфо**](pf-parserdllinfo.md) , содержащую всю информацию, которую сетевой монитор требуется для установки библиотеки DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="ff466-106">When **ParserAutoInstallInfo** is called, the parser returns a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure containing all the information that Network Monitor needs to install a parser DLL.</span></span>

> [!Note]  
> <span data-ttu-id="ff466-107">Сетевой монитор сохраняет список существующих парсеров в файле [*Parser.ini*](p.md) и создает отдельный ini-файл для каждого установленного средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="ff466-107">Network Monitor keeps a list of existing parsers in the [*Parser.ini*](p.md) file, and creates a separate INI file for each installed parser.</span></span>

 

<span data-ttu-id="ff466-108">В процессе установки библиотека DLL средства синтаксического анализа должна выявляет следующее:</span><span class="sxs-lookup"><span data-stu-id="ff466-108">During the installation process, the parser DLL must identify the following:</span></span>

-   <span data-ttu-id="ff466-109">Количество синтаксических анализаторов в библиотеке DLL, включая имя и описание комментария для каждого средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="ff466-109">The number of parsers in the DLL—including a name and comment description for each parser.</span></span>
-   <span data-ttu-id="ff466-110">Протоколы, предшествующие протоколу синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="ff466-110">The protocols that precede the parser protocol.</span></span>
-   <span data-ttu-id="ff466-111">Протоколы, которые следуют за протоколом анализатора.</span><span class="sxs-lookup"><span data-stu-id="ff466-111">The protocols that follow the parser protocol.</span></span>

> [!Note]  
> <span data-ttu-id="ff466-112">Сетевой монитор использует приведенные выше и следующие сведения о протоколе синтаксического анализатора для обновления [*переданных наборов*](h.md) и [*следования наборам*](f.md) синтаксических анализаторов, которые идентифицирует DLL-библиотека синтаксического анализатора.</span><span class="sxs-lookup"><span data-stu-id="ff466-112">Network Monitor uses the preceding and following parser protocol information to update the [*handoff sets*](h.md) and [*follow sets*](f.md) of parsers that your parser DLL identifies.</span></span>

 

<span data-ttu-id="ff466-113">Следующая процедура определяет шаги, необходимые для реализации [**парсераутоинсталлинфо**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ff466-113">The following procedure identifies the steps necessary to implement [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span>

<span data-ttu-id="ff466-114">**Реализация Парсераутоинсталлинфо**</span><span class="sxs-lookup"><span data-stu-id="ff466-114">**To implement ParserAutoInstallInfo**</span></span>

1.  <span data-ttu-id="ff466-115">Выделите структуру [**\_ парсердллинфо PF**](pf-parserdllinfo.md) с помощью **хеапаллок**.</span><span class="sxs-lookup"><span data-stu-id="ff466-115">Allocate a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure using **HeapAlloc**.</span></span>
2.  <span data-ttu-id="ff466-116">Верните память в кучу с помощью **хеапфри**.</span><span class="sxs-lookup"><span data-stu-id="ff466-116">Return memory to the heap using **HeapFree**.</span></span>
3.  <span data-ttu-id="ff466-117">Имейте в виду, что этот вызов также должен выделить структуру [**PF \_ парсеринфо**](pf-parserinfo.md) для каждого средства синтаксического анализа в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="ff466-117">Be aware that this call must also allocate a [**PF\_PARSERINFO**](pf-parserinfo.md) structure for each parser in the DLL.</span></span>
4.  <span data-ttu-id="ff466-118">Укажите количество парсеров (обычно одно), которые библиотека DLL содержит в члене **нпарсерс** в [**PF \_ парсердллинфо**](pf-parserdllinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ff466-118">Specify the number of parsers (typically one) that the DLL contains in the **nParsers** member of [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md).</span></span>
5.  <span data-ttu-id="ff466-119">Укажите имя, комментарий и дополнительный файл справки в элементах **сзпротоколнаме**, **сзкоммент** и **сзелпфиле** каждой структуры [**PF \_ парсеринфо**](pf-parserinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ff466-119">Specify a name, comment, and optional Help file in the **szProtocolName**, **szComment**, and **szHelpFile** members of each [**PF\_PARSERINFO**](pf-parserinfo.md) structure.</span></span>
6.  <span data-ttu-id="ff466-120">Укажите протоколы, которые предшествуют каждому протоколу DLL.</span><span class="sxs-lookup"><span data-stu-id="ff466-120">Specify the protocols that precede each DLL protocol.</span></span> <span data-ttu-id="ff466-121">Одно из следующих условий применяется к входящему поступающему набору.</span><span class="sxs-lookup"><span data-stu-id="ff466-121">One of the following conditions applies to an incoming handoff set.</span></span>
    -   <span data-ttu-id="ff466-122">Если указанные выше протоколы могут определить, что протокол следует за данными в предыдущих протоколах, установите член **пвхохандсоффтоме** в папке [**PF \_ парсеринфо**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ff466-122">If the preceding protocols can determine that your protocol follows from data in the preceding protocols, set the **pWhoHandsOffToMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="ff466-123">В этом случае ваш протокол добавляется к переданным [*наборам*](h.md) предыдущих протоколов.</span><span class="sxs-lookup"><span data-stu-id="ff466-123">In this case, your protocol is then added to the [*handoff sets*](h.md) of the preceding protocols.</span></span>
    -   <span data-ttu-id="ff466-124">Если указанные выше протоколы не могут определить, что протокол соответствует данным в предыдущих протоколах, установите член **пвхоканпрецедеме** в папке [**PF \_ парсеринфо**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ff466-124">If the preceding protocols cannot determine that your protocol follows from data in the preceding protocols, set **pWhoCanPrecedeMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="ff466-125">В этом случае ваш протокол добавляется к следующим [*наборам*](f.md) протоколов.</span><span class="sxs-lookup"><span data-stu-id="ff466-125">In this case, the your protocol is then added to the [*follow sets*](f.md) of the protocols.</span></span>
7.  <span data-ttu-id="ff466-126">Укажите протоколы, которые следуют каждому протоколу DLL.</span><span class="sxs-lookup"><span data-stu-id="ff466-126">Specify the protocols that follow each DLL protocol.</span></span> <span data-ttu-id="ff466-127">Одно из следующих условий применяется к исходящему последующему набору.</span><span class="sxs-lookup"><span data-stu-id="ff466-127">One of the following conditions applies to an outgoing follow-set.</span></span>
    -   <span data-ttu-id="ff466-128">Если ваш протокол может определить, какие протоколы следует использовать в соответствии с данными в протоколе, установите член **пвходоихандоффто** в папке [**PF \_ парсеринфо**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ff466-128">If your protocol can determine which protocols follow based on data in your protocol, set the **pWhoDoIHandOffTo** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="ff466-129">В этом случае эти протоколы добавляются в переданный [*набор*](h.md) протоколов.</span><span class="sxs-lookup"><span data-stu-id="ff466-129">In this case, the these protocols are added to the [*handoff set*](h.md) of your protocols.</span></span>
    -   <span data-ttu-id="ff466-130">Если протокол не может определить, какие протоколы следует использовать в соответствии с данными в протоколе, установите член **пвхоканфолловме** в папке [**PF \_ парсеринфо**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ff466-130">If your protocol cannot determine which protocols follow based on data in your protocol, set the **pWhoCanFollowMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="ff466-131">В этом случае эти протоколы добавляются в [*следующий набор*](f.md) протокола.</span><span class="sxs-lookup"><span data-stu-id="ff466-131">In this case, these protocols are added to the [*follow set*](f.md) of your protocol.</span></span>
8.  <span data-ttu-id="ff466-132">Верните структуру [**\_ парсердллинфо PF**](pf-parserdllinfo.md) в сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="ff466-132">Return the [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure to Network Monitor.</span></span>

<span data-ttu-id="ff466-133">Ниже приведена базовая реализация [**парсераутоинсталлинфо**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ff466-133">The following is a basic implementation of [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span> <span data-ttu-id="ff466-134">Пример кода берется из общего средства синтаксического анализа, которое сетевой монитор предоставляет.</span><span class="sxs-lookup"><span data-stu-id="ff466-134">The code example is taken from the generic parser that Network Monitor provides.</span></span>

``` syntax
#include <windows.h>

PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo() 
{

  /////////////////////////////////////////////////////////////////
  //
  // Allocate memory for PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  PPF_PARSERDLLINFO pParserDllInfo; 
  PPF_PARSERINFO    pParserInfo;
  DWORD NumProtocols;
        DWORD NumParsers;
        DWORD NumFollows;
  NumParsers = 1;
  
  pParserDllInfo = (PPF_PARSERDLLINFO)HeapAlloc( GetProcessHeap(),
                                                 HEAP_ZERO_MEMORY,
                                                 sizeof( PF_PARSERDLLINFO ) +
                                                 NumParsers * sizeof( PF_PARSERINFO) );
  if( pParserDllInfo == NULL)
  {
    return NULL;
  }
  

    
  /////////////////////////////////////////////////////////////////
  //
  // Specify the number of parsers in the DLL.
  //
  /////////////////////////////////////////////////////////////////
  
  pParserDllInfo->nParsers = NumParsers;
  

  /////////////////////////////////////////////////////////////////
  // 
  // Specify the name, comment, and Help file for each protocol.
  // 
  /////////////////////////////////////////////////////////////////
  pParserInfo = &(pParserDllInfo->ParserInfo[0]);
  sprintf_s( pParserInfo->szProtocolName, MAX_PROTOCOL_NAME_LEN, 
    "TestProtocol" );
  sprintf_s( pParserInfo->szComment, MAX_PROTOCOL_COMMENT_LEN,
    "Test protocol for SDK" );
  sprintf_s( pParserInfo->szHelpFile, MAX_PATH, "");
  

  
  /////////////////////////////////////////////////////////////////
  //
  // Specify preceding protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_HANDOFFSET    pHandoffSet;
  PPF_HANDOFFENTRY  pHandoffEntry;
  
  // Allocate PF_HANDOFFSET structure.
  NumHandoffs = 1;                   
  pHandoffSet = (PPF_HANDOFFSET)HeapAlloc( GetProcessHeap(),
                                           HEAP_ZERO_MEMORY,
                                           sizeof( PF_HANDOFFSET ) +
                                           NumHandoffs * sizeof( PF_HANDOFFENTRY) );
  if( pHandoffSet == NULL )
  {
     return pParserDllInfo;
  }

  // Fill in handoff set
  pParserInfo->pWhoHandsOffToMe = pHandoffSet;
  pHandoffSet->nEntries = NumHandoffs;

  // TCP PORT FFFF
  pHandoffEntry = &(pHandoffSet->Entry[0]);
  sprintf_s( pHandoffEntry->szIniFile, MAX_PATH, "TCPIP.INI" );
  sprintf_s( pHandoffEntry->szIniSection, MAX_PATH, "TCP_HandoffSet" );
  sprintf_s( pHandoffEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, 
    "BLRPLATE" );
  pHandoffEntry->dwHandOffValue =        0xFFFF;
  pHandoffEntry->ValueFormatBase =       HANDOFF_VALUE_FORMAT_BASE_DECIMAL;    
  
  

  /////////////////////////////////////////////////////////////////
  //
  // Specify the following protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_FOLLOWSET     pFollowSet;
  PPF_FOLLOWENTRY   pFollowEntry;
 
  // Allocate PF_FOLLOWSET structure
  NumFollows = 1;
  pFollowSet = (PPF_FOLLOWSET)HeapAlloc( GetProcessHeap(),
                                         HEAP_ZERO_MEMORY,
                                         sizeof( PF_FOLLOWSET ) +
                                         NumFollows * sizeof( PF_FOLLOWENTRY) );
  if( pFollowSet == NULL )
  {
    return pParserDllInfo;
  }

  // Fill in the follow set
  pParserInfo->pWhoCanFollowMe = pFollowSet;
  pFollowSet->nEntries = NumFollows;

  // Add SMB
  pFollowEntry = &(pFollowSet->Entry[0]);
  sprintf_s( pFollowEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, "SMB" );
  


  /////////////////////////////////////////////////////////////////
  //
  // Return the PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  return pParserDllInfo;

}
```

 

 



