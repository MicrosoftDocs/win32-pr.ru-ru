---
description: Вызывает функцию Аттачпропертиес для отображения свойств, которые существуют в части распознанных данных.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Реализация Аттачпропертиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673423"
---
# <a name="implementing-attachproperties"></a>Реализация Аттачпропертиес

Сетевой монитор вызывает функцию [**аттачпропертиес**](attachproperties.md) для отображения свойств, которые существуют в части распознанных данных. Функция [**аттачпропертиес**](attachproperties.md) сопоставляет свойства с конкретным расположением.

Для анализа данных в кадре сетевой монитор используется следующий процесс.

-   Во-первых, сетевой монитор вызывает [рекогнизефраме](recognizeframe.md) для распознавания всех протоколов, имеющихся в кадре.
-   Затем сетевой монитор вызывает [**аттачпропертиес**](attachproperties.md) для каждого средства синтаксического анализа, распознающего фрагмент данных.

Когда сетевой монитор вызывает функцию [аттачпропертиес](attachproperties.md) для распознаваемых данных, средство синтаксического анализа, которое вызывается, должно анализировать данные, а затем сопоставлять каждое существующее свойство с расположением в распознанных данных. Средство синтаксического анализа определяет, какие свойства существуют, и где каждое свойство находится в данных. На следующем рисунке показаны распознаваемые синтаксическим анализатором данные.

![данные, распознаваемые синтаксическим анализатором](images/attachproperties1.png)

Во время реализации [**аттачпропертиес**](attachproperties.md)необходимо вызвать одну из следующих функций для каждого свойства, существующего в кадре данных.

-   Вызовите функцию [**аттачпропертинстанцеекс**](attachpropertyinstanceex.md) , если требуется изменить данные свойства в кадре.
-   Вызовите функцию [**аттачпропертинстанце**](attachpropertyinstance.md) , если не хотите изменять данные свойства в кадре.

> [!Note]  
> Рекомендуется использовать данные в том виде, в котором они существуют в записи.

 

Следующая процедура определяет шаги, необходимые для реализации [**аттачпропертиес**](attachproperties.md).

**Реализация Аттачпропертиес**

1.  Определите, какие свойства существуют, и расположение свойства в данных.
2.  Вызовите [**аттачпропертинстанцеекс**](attachpropertyinstanceex.md) для каждого свойства со значением, которое необходимо изменить.
3.  Вызовите [**аттачпропертинстанце**](attachpropertyinstance.md) для каждого свойства со значением, которое не нужно изменять. Как правило, это единственная функция, которую необходимо вызвать.

Ниже приведена базовая реализация [**аттачпропертиес**](attachproperties.md). Имейте в виду, что в примере не содержится код, определяющий, какие свойства существуют, или код для обнаружения свойств.

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



