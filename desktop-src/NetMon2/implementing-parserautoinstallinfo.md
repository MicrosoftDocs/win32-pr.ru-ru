---
description: Сетевой монитор использует функцию экспорта Парсераутоинсталлинфо для установки средства синтаксического анализа. При вызове Парсераутоинсталлинфо средство синтаксического анализа возвращает структуру PF \_ парсердллинфо, содержащую всю информацию, которую сетевой монитор требуется для установки библиотеки DLL средства синтаксического анализа.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Реализация Парсераутоинсталлинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d1c797f53ad110392fea304cc0a610fdb0f9346c745e2f7dea2bff16208e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743084"
---
# <a name="implementing-parserautoinstallinfo"></a>Реализация Парсераутоинсталлинфо

Сетевой монитор использует функцию экспорта [**парсераутоинсталлинфо**](parserautoinstallinfo.md) для установки средства синтаксического анализа. При вызове **парсераутоинсталлинфо** средство синтаксического анализа возвращает структуру [**PF \_ парсердллинфо**](pf-parserdllinfo.md) , содержащую всю информацию, которую сетевой монитор требуется для установки библиотеки DLL средства синтаксического анализа.

> [!Note]  
> Сетевой монитор сохраняет список существующих парсеров в файле [*Parser.ini*](p.md) и создает отдельный ini-файл для каждого установленного средства синтаксического анализа.

 

В процессе установки библиотека DLL средства синтаксического анализа должна выявляет следующее:

-   Количество синтаксических анализаторов в библиотеке DLL, включая имя и описание комментария для каждого средства синтаксического анализа.
-   Протоколы, предшествующие протоколу синтаксического анализа.
-   Протоколы, которые следуют за протоколом анализатора.

> [!Note]  
> Сетевой монитор использует приведенные выше и следующие сведения о протоколе синтаксического анализатора для обновления [*переданных наборов*](h.md) и [*следования наборам*](f.md) синтаксических анализаторов, которые идентифицирует DLL-библиотека синтаксического анализатора.

 

Следующая процедура определяет шаги, необходимые для реализации [**парсераутоинсталлинфо**](parserautoinstallinfo.md).

**Реализация Парсераутоинсталлинфо**

1.  Выделите структуру [**\_ парсердллинфо PF**](pf-parserdllinfo.md) с помощью **хеапаллок**.
2.  Верните память в кучу с помощью **хеапфри**.
3.  Имейте в виду, что этот вызов также должен выделить структуру [**PF \_ парсеринфо**](pf-parserinfo.md) для каждого средства синтаксического анализа в библиотеке DLL.
4.  Укажите количество парсеров (обычно одно), которые библиотека DLL содержит в члене **нпарсерс** в [**PF \_ парсердллинфо**](pf-parserdllinfo.md).
5.  Укажите имя, комментарий и дополнительный файл справки в элементах **сзпротоколнаме**, **сзкоммент** и **сзелпфиле** каждой структуры [**PF \_ парсеринфо**](pf-parserinfo.md) .
6.  Укажите протоколы, которые предшествуют каждому протоколу DLL. Одно из следующих условий применяется к входящему поступающему набору.
    -   Если указанные выше протоколы могут определить, что протокол следует за данными в предыдущих протоколах, установите член **пвхохандсоффтоме** в папке [**PF \_ парсеринфо**](pf-parserinfo.md). В этом случае ваш протокол добавляется к переданным [*наборам*](h.md) предыдущих протоколов.
    -   Если указанные выше протоколы не могут определить, что протокол соответствует данным в предыдущих протоколах, установите член **пвхоканпрецедеме** в папке [**PF \_ парсеринфо**](pf-parserinfo.md). В этом случае ваш протокол добавляется к следующим [*наборам*](f.md) протоколов.
7.  Укажите протоколы, которые следуют каждому протоколу DLL. Одно из следующих условий применяется к исходящему последующему набору.
    -   Если ваш протокол может определить, какие протоколы следует использовать в соответствии с данными в протоколе, установите член **пвходоихандоффто** в папке [**PF \_ парсеринфо**](pf-parserinfo.md). В этом случае эти протоколы добавляются в переданный [*набор*](h.md) протоколов.
    -   Если протокол не может определить, какие протоколы следует использовать в соответствии с данными в протоколе, установите член **пвхоканфолловме** в папке [**PF \_ парсеринфо**](pf-parserinfo.md). В этом случае эти протоколы добавляются в [*следующий набор*](f.md) протокола.
8.  Верните структуру [**\_ парсердллинфо PF**](pf-parserdllinfo.md) в сетевой монитор.

Ниже приведена базовая реализация [**парсераутоинсталлинфо**](parserautoinstallinfo.md). Пример кода берется из общего средства синтаксического анализа, которое сетевой монитор предоставляет.

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

 

 



