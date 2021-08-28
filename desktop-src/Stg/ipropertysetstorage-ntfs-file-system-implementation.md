---
title: IPropertySetStorage — реализация файловой системы NTFS
description: NTFS версии 5,0 обеспечивает реализацию IPropertySetStorage для файлов на томе NTFS, если сами файлы не являются составными файлами.
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Стрктд STG, реализации, файловая система NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0794e2905cd9e8bd06804decb756b3f1f639c75e837b2d5f3181bb73939717f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683044"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>IPropertySetStorage — реализация файловой системы NTFS

NTFS версии 5,0 обеспечивает реализацию [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) для файлов на томе NTFS, если сами файлы не являются составными файлами. Реализация NTFS эквивалентна [реализации составного файла](ipropertysetstorage-compound-file-implementation.md). Дополнительные сведения об исключениях см. в разделе Примечания.

**Получение указателя на реализацию IPropertySetStorage в NTFS**

1.  Вызовите [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) и укажите **стгфмт- \_ файл** в параметре *грффлагс* , чтобы создать новый файл.
2.  Вызовите [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) и укажите либо **стгфмт \_ File** , либо **стгфмт \_ любое** значение перечисления в параметре *грффлагс* , чтобы открыть существующий файл.

Однако невозможно получить реализацию [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) для NTFS для составного файла. При открытии составного файла с помощью [**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)указание значения **перечисления \_ файлов стгфмт** приводит к ошибке.

Кроме того, простые наборы свойств не могут быть транзакционными. Это значит, что нельзя указать **стгм в \_ транзакции** в параметре *Грфмоде* методов [**CREATE**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) и [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , если в параметре *грффлагс* не указано значение **пропсетфлаг \_ unsimple** . Сам объект "набор свойств" не поддерживает обработку транзакций.

## <a name="when-to-use"></a>Назначение

Вызовите методы [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) для создания, открытия или удаления наборов свойств в текущем хранилище набора свойств NTFS. Существует также метод [**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), который предоставляет указатель на перечислитель, который можно использовать для перечисления наборов свойств в хранилище.

## <a name="compatibility"></a>Совместимость

реализации [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) и [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в NTFS доступны начиная с Windows 2000. Более ранние версии не могут получить доступ к этим наборам свойств.

В реализации NTFS наборы свойств хранятся в альтернативных потоках файла NTFS. При копировании основного файла необходимо скопировать альтернативные потоки.

> [!Caution]  
> Не все файловые системы поддерживают такие потоки. Если файл NTFS с наборами свойств копируется на том FAT, копируются только данные из этого файла. набор свойств потерян. Функция [**CopyFile**](/windows/desktop/api/winbase/nf-winbase-copyfile) не возвращает ошибку в этом случае.

 

> [!Caution]  
> если компьютер, на котором выполняется копирование файлов, не является компьютером, работающим на Windows 2000 или более поздней версии, наборы свойств могут быть потеряны. например, если компьютер, работающий под управлением операционной системы Windows 95, копирует файл NTFS, набор свойств будет потерян, даже если файл назначения также находится на томе NTFS.

 

## <a name="methods"></a>Методы

Реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) в файловой системе NTFS поддерживает следующие методы.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Создает новое свойство, заданное в текущем хранилище файлов NTFS и, при возвращении, предоставляет указатель интерфейса на реализацию файла [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) NTFS. Режим общего доступа, указанный в параметре *грфмоде* , должен быть **стгм \_ \_ монопольным**.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Открывает существующее свойство, установленное в текущем хранилище свойств. При возврате он предоставляет указатель интерфейса на реализацию файла NTFS [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Режим общего доступа, указанный в параметре *грфмоде* , должен быть **стгм \_ \_ монопольным**.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D удалить**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Удаляет свойство, заданное в текущем хранилище свойств.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Создает объект, используемый для перечисления структур [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Каждая структура **статпропсетстг** предоставляет данные об отдельном наборе свойств.

</dd> </dl>

## <a name="remarks"></a>Remarks

Реализации наборов свойств хранилища [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) и [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в файловой системе NTFS не влияют на содержимое этого файла. Например, если создать свойство, заданное в HTML-файле с именем Default.htm, этот файл по-прежнему будет отображаться правильно в браузере. Это значит, что изменения в файле, использующие эти два интерфейса, не обнаруживаются при доступе к файлу с помощью функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

Реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) в NTFS обеспечивает надежную реализацию при использовании для записи наборов свойств в файл на томе NTFS версии 5,0. Такие наборы свойств не могут быть повреждены реализацией даже в случае сбоя системы. Например, если произошел сбой системы во время вызова [**ипропертистораже:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) , пока набор свойств сбрасывается на диск, набор свойств никогда не остается в промежуточном состоянии. Либо будет сохранена Предыдущая версия набора свойств, либо все обновления будут сохранены.

Реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) в NTFS отличается от реализации составного файла следующими способами:

-   Структура [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , полученная из интерфейса [**иенумстатпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , содержит элемент **CLSID** , значение которого всегда равно нулю (**CLSID \_ null**). при реализации составного файла правильный элемент **clsid** возвращается для непростых (см. [служба хранилища и объекты потока для наборов свойств](storage-vs--stream-for-a-property-set.md)).
-   При получении реализации [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) интерфейса для NTFS с помощью функции [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) или [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) параметр *грфмоде* должен соответствовать тем же правилам, что и для реализации составного файла.

    Кроме того, нельзя использовать следующие флаги:

    **Стгм \_ SIMPLE**, **стгм \_ транзакционный**, **стгм \_ Convert**, **стгм \_ Priority** и **стгм \_ делетеонрелеасе**.

-   Когда интерфейс [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) для NTFS получает функции [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) или [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , режимы общего доступа применяются в основном к другим экземплярам этого интерфейса, а не к экземплярам, открывающим сам файл. Например, если интерфейс NTFS **IPropertySetStorage** открыт путем вызова функции **стгопенсторажеекс** , а для параметра *грфмоде* задано значение **стгм \_ ReadWrite стгм в \| \_ \_ монопольном доступе**, файл можно открыть с помощью функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

    Такие одновременные экземпляры открытия этого интерфейса подвергаются следующим ограничениям: параметр *двшаремоде* в функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) должен указывать флаг **\_ \_ чтения общей папки** , а параметр *двакцесс* не должен указывать флаг **Delete** . Кроме того, функции [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) и [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) не должны вызываться для файла, для которого открыты эти интерфейсы набора свойств, так как эти функции нуждаются в доступе к файлу для **удаления** .

-   Если метод [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) для NTFS открыт только для чтения, а в файле в настоящее время нет наборов свойств, то возвращаемый объект на самом деле не удерживает открытия файла. Следовательно, другие вакансии этого файла будут выполнены, даже если режим общего доступа исходной операции открытия в противном случае отклонит его.

    Например Если [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS открывается в режиме **стгм \_ Read \| стгм \_ \_ монопольного доступа**, а файл не имеет наборов свойств, можно одновременно открыть файл **стгм \_ ReadWrite \| стгм в \_ \_ монопольном доступе**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ипропертистораже — реализация файловой системы NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: Енумелементс**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Константы ПРОПСЕТФЛАГ**](propsetflag-constants.md)
</dt> <dt>

[**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 