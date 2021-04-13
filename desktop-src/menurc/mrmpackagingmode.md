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
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340740"
---
# <a name="mrmpackagingmode-enumeration"></a>Перечисление Мрмпаккагингмоде

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1803\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только классические приложения Windows Server\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Мрмресаурцеиндексер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

