---
description: 'В API теневого копирования томов определены следующие типы данных:'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Типы данных API теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809838"
---
# <a name="volume-shadow-copy-api-data-types"></a>Типы данных API теневого копирования томов

В API теневого копирования томов определены следующие типы данных:

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>\_идентификатор VSS
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

Определение **\_ идентификатора VSS** указывает общий формат идентификатора VSS. **\_ Идентификатор VSS** является стандартным типом данных GUID.

Служба **VSS \_ ИДЕНТИФИКАТОРы** используются для идентификации следующих объектов: теневые копии, наборы теневых копий, поставщики, версии поставщиков, модули записи (идентификатор класса модуля записи) и экземпляры модулей записи.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>\_ПВСЗ VSS
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

Определение **\_ Пвсз для VSS** указывает строку расширенных символов, заканчивающуюся нулем (WChar).

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>\_Метка времени VSS
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

Определение **\_ метки времени VSS** содержит сведения о временной метке в виде 64-разрядного целого числа, содержащего число 100-наносекундных интервалов, прошедших с 1 января 1601 (UTC). Это определение является взаимозаменяемым с структурой [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> </dl>

 

 
