---
title: version_stamp Switch
description: '\_Параметр метки/Version подавляет создание макросов, указывающих минимальный необходимый номер версии файла заголовка RPC, рпкндр. h.'
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp параметр MIDL
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105681543"
---
# <a name="version_stamp-switch"></a>\_параметр метки/Version

Параметр **\_ метки/Version** подавляет создание макросов, указывающих минимальный необходимый номер версии файла заголовка RPC, рпкндр. h.

Новые возможности MIDL могут потребовать, чтобы дополнительные определения правильно компилируют заглушку, поэтому заглушка содержит макросы, которые проверяют совместимость двоичных файлов MIDL и среды сборки. Этот параметр может потребоваться использовать при перемещении MIDL в среду построения, отличную от среды, в которой сначала были установлены двоичные файлы MIDL.

Обратите внимание, что смешивание сред сборки не поддерживается.

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a>Параметры коммутатора

Этот параметр не имеет параметров.

 

 




