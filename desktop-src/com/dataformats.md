---
title: DataFormats
description: Указывает форматы данных по умолчанию и основные параметры, поддерживаемые приложением.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Формат COM раздела реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb8b2cc2ad4d11137fa41f419db2184f1a2b47fb850176227401e3d2b1aec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310602"
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

## <a name="remarks"></a>Remarks

Значение *File/Format* указывает основной файл или формат объекта по умолчанию для объектов этого класса.

Значение *formats* указывает список форматов для реализаций по умолчанию [**енумформатетк**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), где *n* — целочисленный индекс, начинающийся с нуля. Например, *n*  =  *Format*, *аспект*, *средний*, *флаг*, где *Формат* — формат буфера обмена, *аспект* — один или несколько членов [**дваспект**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *средний* — один или несколько членов [**тимед**](/windows/win32/api/objidl/ne-objidl-tymed), а *флаг* — один или несколько элементов [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IDataObject:: Енумформатетк**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject:: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




