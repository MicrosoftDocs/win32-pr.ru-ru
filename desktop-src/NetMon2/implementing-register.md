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
# <a name="implementing-register"></a><span data-ttu-id="f1f3f-104">Реализация регистра</span><span class="sxs-lookup"><span data-stu-id="f1f3f-104">Implementing Register</span></span>

<span data-ttu-id="f1f3f-105">Сетевой монитор загружает запись из файла записи, а затем запускает вызов функции [**Register**](register-parser.md) для всех протоколов, которые она может опознать.</span><span class="sxs-lookup"><span data-stu-id="f1f3f-105">Network Monitor loads a capture from the capture file, and then starts calling the [**Register**](register-parser.md) function for all the protocols that it can identify.</span></span> <span data-ttu-id="f1f3f-106">Каждая библиотека DLL анализатора должна реализовать функцию **Register** для каждого протокола, ПОДДЕРЖИВАЕМого библиотекой DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="f1f3f-106">Each parser DLL must implement a **Register** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="f1f3f-107">Каждая реализация функции [**Register**](register-parser.md) должна вызывать функции [**креатепропертидатабасе**](createpropertydatabase.md) и [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) для создания и заполнения [*базы данных свойств*](p.md) протокола, а затем [**креатехандоффтабле**](createhandofftable.md) для создания [*таблицы*](h.md) передачи для протокола — при необходимости.</span><span class="sxs-lookup"><span data-stu-id="f1f3f-107">Each implementation of the [**Register**](register-parser.md) function must call the [**CreatePropertyDatabase**](createpropertydatabase.md) and [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) functions to create and fill-in the [*property database*](p.md) for the protocol, and then the [**CreateHandoffTable**](createhandofftable.md) to create the [*handoff table*](h.md) for the protocol — if needed.</span></span>

> [!Note]  
> <span data-ttu-id="f1f3f-108">Свойства протокола определяются для сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="f1f3f-108">Protocol properties are defined for Network Monitor.</span></span> <span data-ttu-id="f1f3f-109">Свойства не сопоставлены с расположением в данных записи, пока не будет вызвана функция экспорта [**аттачпропертиес**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="f1f3f-109">Properties are not mapped to a location in a capture data until the [**AttachProperties**](attachproperties.md) export function is called.</span></span>

 

<span data-ttu-id="f1f3f-110">Следующая процедура определяет шаги, необходимые для реализации функции [**Register**](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="f1f3f-110">The following procedure identifies the steps necessary to implement the [**Register**](register-parser.md) function.</span></span>

<span data-ttu-id="f1f3f-111">**Реализация регистрации для одного протокола**</span><span class="sxs-lookup"><span data-stu-id="f1f3f-111">**To implement Register for one protocol**</span></span>

1.  <span data-ttu-id="f1f3f-112">Определите массив структур [**PROPERTYINFO**](propertyinfo.md) , чтобы описать каждое свойство, поддерживаемое протоколом.</span><span class="sxs-lookup"><span data-stu-id="f1f3f-112">Define an array of [**PROPERTYINFO**](propertyinfo.md) structures to describe each property that the protocol supports.</span></span>
2.  <span data-ttu-id="f1f3f-113">Вызовите [**креатепропертидатабасе**](createpropertydatabase.md) , чтобы предоставить маркер протокола, и число свойств, которое поддерживает протокол.</span><span class="sxs-lookup"><span data-stu-id="f1f3f-113">Call [**CreatePropertyDatabase**](createpropertydatabase.md) to provide a protocol handle, and the number of properties that the protocol supports.</span></span>
3.  <span data-ttu-id="f1f3f-114">Вызовите [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) в цикле, чтобы добавить каждое свойство, определенное в массиве структуры [**PROPERTYINFO**](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f1f3f-114">Call [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in a loop to add each property defined in the [**PROPERTYINFO**](propertyinfo.md) structure array.</span></span>
4.  <span data-ttu-id="f1f3f-115">Если протокол использует переданную таблицу, вызовите [**креатехандоффтабле**](createhandofftable.md), после того как все свойства протокола будут добавлены в базу данных свойств.</span><span class="sxs-lookup"><span data-stu-id="f1f3f-115">If the protocol uses a handoff table, call [**CreateHandoffTable**](createhandofftable.md)— after all the properties of the protocol are added to the property database.</span></span>

<span data-ttu-id="f1f3f-116">Ниже приведена базовая реализация [**Register**](register-parser.md).</span><span class="sxs-lookup"><span data-stu-id="f1f3f-116">The following is a basic implementation of [**Register**](register-parser.md).</span></span> <span data-ttu-id="f1f3f-117">Обратите внимание, что для протокола, поддерживающего только два свойства, создается база данных свойств.</span><span class="sxs-lookup"><span data-stu-id="f1f3f-117">Note that a property database is created for a protocol that supports only two properties.</span></span> <span data-ttu-id="f1f3f-118">Этот пример кода взят из общего средства синтаксического анализа, которое сетевой монитор предоставляет.</span><span class="sxs-lookup"><span data-stu-id="f1f3f-118">This code example is taken from the generic parser that Network Monitor provides.</span></span>

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

 

 
