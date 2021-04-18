---
title: DataFormats
description: Указывает форматы данных по умолчанию и основные параметры, поддерживаемые приложением.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Формат COM раздела реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700697"
---
# <a name="dataformats"></a>DataFormats

Указывает форматы данных по умолчанию и основные параметры, поддерживаемые приложением.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a>Комментарии

Значение *File/Format* указывает основной файл или формат объекта по умолчанию для объектов этого класса.

Значение *formats* указывает список форматов для реализаций по умолчанию [**енумформатетк**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), где *n* — целочисленный индекс, начинающийся с нуля. Например, *n*  =  *Format*, *аспект*, *средний*, *флаг*, где *Формат* — формат буфера обмена, *аспект* — один или несколько членов [**дваспект**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *средний* — один или несколько членов [**тимед**](/windows/win32/api/objidl/ne-objidl-tymed), а *флаг* — один или несколько элементов [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IDataObject:: Енумформатетк**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject:: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




