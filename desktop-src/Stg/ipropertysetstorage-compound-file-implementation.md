---
title: Реализация файла IPropertySetStorage-Compound
description: Реализация объекта хранилища составных файлов COM включает реализацию Ипропертистораже, интерфейс, управляющий одним набором постоянных свойств, и IPropertySetStorage, интерфейс, который управляет группами постоянных наборов свойств.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Стрктд STG, реализации, составной файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9053a7cf6bf1ae7e4230b15eb0117c428acb08da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792961"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>Реализация файла IPropertySetStorage-Compound

[Реализация объекта хранилища составных файлов com](ipropertystorage-compound-file-implementation.md) включает реализацию [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), интерфейс, управляющий одним набором постоянных свойств, и [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), интерфейс, который управляет группами постоянных наборов свойств.

Чтобы получить указатель на реализацию составного файла [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), укажите определенное в заголовке имя идентификатора IID \_ IStorage в качестве параметра *riid* или используйте функции [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) или [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . В обоих случаях укажите хранилище СТГФМТ в \_ качестве параметра *стгфмт* . (СТГФМТ \_ Можно также указать ANY в случае **стгопенсторажеекс**.) Кроме того, укажите определенное заголовком Имя идентификатора интерфейса (IID) IID \_ IPropertySetStorage в качестве параметра *riid* . Обе функции предоставляют указатель на интерфейс **IPropertySetStorage** объекта.

Другим способом получения указателя на реализацию составного файла является указание определенного по заголовку имени для идентификатора IID \_ IStorage в качестве параметра *riid* или использование функций [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) или [**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) . При этом будет предоставлен указатель на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) объекта. Если вы хотите работать с постоянными наборами свойств, вызовите метод [**IStorage:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для интерфейса [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

## <a name="when-to-use-ipropertysetstorage"></a>Когда следует использовать IPropertySetStorage

Вызовите методы [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , чтобы создавать, открывать или удалять наборы свойств в текущем составном наборе свойств, заданных в хранилище. Существует также метод [**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), который предоставляет указатель на перечислитель, который можно использовать для перечисления наборов свойств в хранилище.

## <a name="methods"></a>Методы

[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Создает новое свойство, установленное в текущем хранилище составных файлов, а при возвращении предоставляет указатель интерфейса на реализацию составного файла [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . В этой реализации наборы свойств могут быть транзакционными, только если \_ указано пропсетфлаг непростое. Для этого метода требуется, чтобы режим общего доступа, заданный в параметре *грфмоде* , был стгм \_ \_ монопольно, а режим доступа — стгм \_ Read или стгм \_ ReadWrite (стгм \_ Write Mode не поддерживается).

[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Открывает существующее свойство, установленное в текущем хранилище свойств. При возврате он предоставляет указатель интерфейса для реализации составного файла, [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Для этого метода требуется, чтобы режим общего доступа, заданный в параметре *грфмоде* , был стгм \_ \_ монопольно, а режим доступа — стгм \_ Read или стгм \_ ReadWrite (стгм \_ Write не поддерживается).

[**IPropertySetStorage::D удалить**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Удаляет свойство, заданное в этом хранилище свойств.

[**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Создает объект, используемый для перечисления структур [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Каждая структура **статпропсетстг** предоставляет данные об отдельном наборе свойств.

## <a name="remarks"></a>Комментарии

Начиная с Windows 2000, реализация составного файла [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) поддерживает простой режим. Простой режим обозначается указанием \_ простого флага стгм для функций [**Стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) и [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Если составной файл открыт в простом режиме, связанная реализация **IPropertySetStorage** ограничена следующим образом:

-   Можно создавать только простые наборы свойств. Это значит, что при указании \_ НЕпростого значения пропсетфлаг в параметре *грффлагс* для метода [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) возникает ошибка.
-   После создания составного файла с помощью [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) с использованием стгм \_ Simple и запроса к интерфейсу [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) можно вызвать [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) один раз. Затем необходимо освободить интерфейс [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) перед повторным вызовом метода **CREATE** . Дополнительные сведения о режиме Simple см. в разделе [**константы стгм**](stgm-constants.md).
-   Метод [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) нельзя использовать для открытия набора свойств после использования [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) для создания объекта хранилища. Вместо этого необходимо использовать [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) перед запросом на [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) и вызовом метода **Open** .
-   После открытия составного файла с [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) с помощью \_ флага стгм Simple и запроса к интерфейсу [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) можно открыть по одному набору свойств за раз с помощью [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open). Кроме того, при открытом наборе свойств может быть невозможно увеличить общий размер набора свойств.

Простые наборы свойств не могут быть транзакционными. Нельзя указать СТГМ \_ в транзакции в параметре *Грфмоде* методов [**CREATE**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) и [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , если в \_ параметре *грффлагс* не указано пропсетфлаг неsimple. Имейте в виду, что простые и непростые наборы свойств не связаны с наборами свойств простого режима, описанными выше. Дополнительные сведения о простых и непростых наборах свойств см. [в разделе объекты хранилища и потока для набора свойств](storage-vs--stream-for-a-property-set.md).

> [!Note]  
> Наборы свойств Документсуммаринформатион и Пользователяопределенные являются уникальными в том, что они могут иметь два раздела набора свойств. Дополнительные сведения см. в описании [наборов свойств документсуммаринформатион и пользователяопределенные](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ипропертистораже — реализация составного файла](ipropertystorage-compound-file-implementation.md)
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

 

 