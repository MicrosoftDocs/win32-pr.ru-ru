---
description: 'Дополнительные сведения: структура JET_CONVERT'
title: Структура JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ce3fbcc7de9c7904689de3df923a87d575b1b92b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986787"
---
# <a name="jet_convert-structure"></a>Структура JET_CONVERT


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_convert-structure"></a>Структура JET_CONVERT

Структура **JET_CONVERT** содержит имя более ранней библиотеки DLL версии ESE, которая используется для чтения баз данных, созданных с использованием более ранней версии. Кроме того, предоставляются другие флаги для управления природой преобразования.

**Windows Server 2003:** функция в [жеткомпакт](./jetcompact-function.md) , которая выполнила преобразование, была удалена из продукта в Windows Server 2003. он поддерживается только в Windows 2000 и Windows XP.

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>Элементы

**сзолддлл**

Имя, включая сведения о пути, к более ранней версии библиотеки DLL ESE.

**ффлагс**

Зарезервировано для системного использования.

**фсчемачанжесонли**

Зарезервировано для системного использования.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JET_CONVERT_W</strong> (Юникод) и <strong>JET_CONVERT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>См. также:

[жеткомпакт](./jetcompact-function.md)
