---
title: Ипропертистораже — реализация файловой системы NTFS
description: В NTFS версии 5,0 имеется реализация интерфейса Ипропертистораже для файлов на томе NTFS, если файлы не являются составными файлами.
ms.assetid: d0ffd975-5bc2-4de3-b0c1-c9188541f46a
keywords:
- Ипропертистораже Стрктд STG, реализации, файловая система NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca359bebbd05e67a034494023d7fc23089396b32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661743"
---
# <a name="ipropertystorage-ntfs-file-system-implementation"></a>Ипропертистораже — реализация файловой системы NTFS

В NTFS версии 5,0 имеется реализация интерфейса [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) для файлов на томе NTFS, если файлы не являются составными файлами.

**Получение указателя на реализацию файловой системы NTFS для IPropertySetStorage**

1.  Вызовите метод [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) с помощью реализации [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)в NTFS.
2.  Вызовите [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) с помощью реализации [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)в NTFS.

## <a name="when-to-use"></a>Назначение

Используйте [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) для управления свойствами в пределах одного набора свойств. Его методы поддерживают чтение, запись и удаление свойств, а также необязательные имена строк, которые могут быть связаны с идентификаторами свойств. Другой метод позволяет задать время, связанное с хранилищем свойств, а другой разрешает назначение идентификатора CLSID, используемого для связывания другого кода, например кода пользовательского интерфейса, с набором свойств. Вызов метода [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) предоставляет указатель на реализацию [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)в NTFS, который позволяет перечислить свойства в наборе.

## <a name="remarks"></a>Комментарии

Реализация NTFS предоставляет практически те же возможности, что и реализация составного файла. Дополнительные сведения см. в разделе [реализация составного файла ипропертистораже](ipropertystorage-compound-file-implementation.md).

Поскольку NTFS является надежной файловой системой, набор свойств NTFS никогда не остается в неправильном состоянии. При записи содержимого [**ИПРОПЕРТИСТОРАЖЕ**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) NTFS в базовый файл NTFS либо все, либо ни одно из этих состояний записывается в файл как атомарная операция, даже если во время операции происходит сбой, например аварийное завершение процесса. Чтобы добиться аналогичного поведения при реализации составного файла, родительский интерфейс [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) должен быть открыт в режиме транзакций.

Этот уровень надежности возможен только при доступе к свойству NTFS, заданному на томе NTFS 5,0. Можно получить доступ к наборам свойств NTFS в более ранних версиях NTFS (например, на компьютере под управлением Windows NT или Windows 2000, который обращается к наборам свойств на компьютере файлового сервера, работающем под управлением Windows NT 4,0), но они не обязательно должны находиться в правильном состоянии в случае непредвиденного сбоя.

Несмотря на то, что реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) в NTFS не поддерживает транзакционную поддержку, реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в NTFS поддерживается. То есть **\_ транзакционная стгм** может быть указана в параметре *Грфмоде* в методах [**CREATE**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) и [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) **IPropertySetStorage**. Как и в реализации составного файла, режим транзакций может быть только для непростых хранилищ свойств (в параметре *грффлагс* указано **пропсетфлаг \_ unsimple** ).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[IPropertySetStorage — реализация файловой системы NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)
</dt> </dl>

 

 