---
title: Перечисление Мрмпаккагингоптионс (Мрмресаурцеиндексер. h)
description: Определяет константы, указывающие параметры для PRI файла, созданного с помощью Мрмкреатересаурцефиле и Мрмкреатересаурцефилеинмемори.
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- Меню перечисления Мрмпаккагингоптионс и другие ресурсы
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede8ef1367bc217827f616514a4fb9ea69e180cb654a19cbbe9593d4c74036d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971973"
---
# <a name="mrmpackagingoptions-enumeration"></a>Перечисление Мрмпаккагингоптионс

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Определяет константы, указывающие параметры для PRI файла, созданного с помощью [**мрмкреатересаурцефиле**](mrmcreateresourcefile.md) и [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md). Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**мрмпаккагингоптионсноне**
</dt> <dd>

Указывает, что параметры упаковки отсутствуют.

</dd> <dt>

<span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**мрмпаккагингоптионсомитсчемафромресаурцепаккс**
</dt> <dd>

Указывает, что необходимо создать пакет ресурсов без схемы.

</dd> <dt>

<span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**мрмпаккагингоптионссплитлангуажевариантс**
</dt> <dd>

Указывает, что PRI-файл должен автоматически разбиваться всеми поддерживаемыми квалификаторами (в частности, языком и масштабом).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1803\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только серверные \[ классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Мрмресаурцеиндексер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

