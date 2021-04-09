---
title: дефаултикон
description: Содержит сведения о значке по умолчанию для однообъектных презентаций.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- COM раздела реестра Дефаултикон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070675"
---
# <a name="defaulticon"></a>дефаултикон

Содержит сведения о значке по умолчанию для однообъектных презентаций.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** , указывающее полный путь к исполняемому файлу приложения объекта и индексу ресурса значка в исполняемом файле.

**Дефаултикон** определяет значок, используемый, если, например, элемент управления сведен к значку. Эта запись содержит полный путь к исполняемому файлу серверного приложения и индексу ресурса значка в исполняемом файле. Приложения могут использовать сведения, предоставляемые **дефаултикон** , для получения маркера значка с помощью [**екстрактикон**](/windows/win32/api/shellapi/nf-shellapi-extracticona).

 

 