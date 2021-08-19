---
title: Перечисление Мрмпаккагингмоде (Мрмресаурцеиндексер. h)
description: Определяет константы, которые определяют тип PRI-файлов, создаваемых Мрмкреатересаурцефиле и Мрмкреатересаурцефилеинмемори.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Меню перечисления Мрмпаккагингмоде и другие ресурсы
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b4e968a43ba08786cc433b199bef5c07431420ac5942646530960279ea853e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870153"
---
# <a name="mrmpackagingmode-enumeration"></a>Перечисление Мрмпаккагингмоде

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Определяет константы, которые определяют тип PRI-файлов, создаваемых [**мрмкреатересаурцефиле**](mrmcreateresourcefile.md) и [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md). Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**мрмпаккагингмодестандалонефиле**
</dt> <dd>

Указывает, что должен быть создан один PRI-файл.

</dd> <dt>

<span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**мрмпаккагингмодеаутосплит**
</dt> <dd>

Указывает, что необходимо создать несколько PRI файлов. Разделите автоматически всеми поддерживаемыми квалификаторами (в частности, языком и масштабом).

</dd> <dt>

<span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**мрмпаккагингмодересаурцепакк**
</dt> <dd>

Указывает, что должен быть создан вспомогательный PRI-файл надстройки.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1803\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только серверные \[ классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Мрмресаурцеиндексер. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

