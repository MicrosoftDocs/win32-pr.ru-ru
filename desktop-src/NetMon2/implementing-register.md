---
description: Сетевой монитор загружает запись из файла записи, а затем запускает вызов функции Register для всех протоколов, которые она может опознать. Каждая библиотека DLL анализатора должна реализовать функцию Register для каждого протокола, поддерживаемого библиотекой DLL средства синтаксического анализа.
ms.assetid: a53c64cb-569f-454b-ae85-7b850228c954
title: Реализация регистра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59f34f5f97925627184db7188aac0a9eb796a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674293"
---
# <a name="implementing-register"></a>Реализация регистра

Сетевой монитор загружает запись из файла записи, а затем запускает вызов функции [**Register**](register-parser.md) для всех протоколов, которые она может опознать. Каждая библиотека DLL анализатора должна реализовать функцию **Register** для каждого протокола, ПОДДЕРЖИВАЕМого библиотекой DLL средства синтаксического анализа.

Каждая реализация функции [**Register**](register-parser.md) должна вызывать функции [**креатепропертидатабасе**](createpropertydatabase.md) и [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) для создания и заполнения [*базы данных свойств*](p.md) протокола, а затем [**креатехандоффтабле**](createhandofftable.md) для создания [*таблицы*](h.md) передачи для протокола — при необходимости.

> [!Note]  
> Свойства протокола определяются для сетевой монитор. Свойства не сопоставлены с расположением в данных записи, пока не будет вызвана функция экспорта [**аттачпропертиес**](attachproperties.md) .

 

Следующая процедура определяет шаги, необходимые для реализации функции [**Register**](register-parser.md) .

**Реализация регистрации для одного протокола**

1.  Определите массив структур [**PROPERTYINFO**](propertyinfo.md) , чтобы описать каждое свойство, поддерживаемое протоколом.
2.  Вызовите [**креатепропертидатабасе**](createpropertydatabase.md) , чтобы предоставить маркер протокола, и число свойств, которое поддерживает протокол.
3.  Вызовите [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) в цикле, чтобы добавить каждое свойство, определенное в массиве структуры [**PROPERTYINFO**](propertyinfo.md) .
4.  Если протокол использует переданную таблицу, вызовите [**креатехандоффтабле**](createhandofftable.md), после того как все свойства протокола будут добавлены в базу данных свойств.

Ниже приведена базовая реализация [**Register**](register-parser.md). Обратите внимание, что для протокола, поддерживающего только два свойства, создается база данных свойств. Этот пример кода взят из общего средства синтаксического анализа, которое сетевой монитор предоставляет.

``` syntax
#include <windows.h>

PROPERTYINFO MyProtocolPropertyTable[]
{
  // Summary property (0)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "Summary",                       // Property label.
     "Summary of protocol packet",    // Property comment.
     PROP_TYPE_SUMMARY,               // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

  // WORD property (1)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "WORD property",                 // Property label.
     "16-bit WORD property",         // Property comment.
     PROP_TYPE_WORD,                  // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

}

void BHAPI MyProtocolRegister( HPPROTOCOL hProtocol) 
{
  // Create property database.
  DWORD dwNumberOfProperties = 2;
  CreatePropertyDatabase (hProtocol,
                          dwNumberOfProperties
                          );
  
  // Add properties to database.
  WORD i;
  for( i=0; i< dwNumberOfProperties; i++)
  {
     AddProperty(hProtocol, &MyProtocolPropertyTable[i]);
  }

  // Create handoff table.
  CreateHandoffTable("myProtocolHandoffTable",
                          "myProtocol.ini",
                           hTable,
                           MaxEntries,
                           10       // Handoff set values are base 10.
                          )
}
```

 

 
