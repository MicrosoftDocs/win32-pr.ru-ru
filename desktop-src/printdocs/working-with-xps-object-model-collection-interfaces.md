---
description: Описывает, как использовать общие методы интерфейсов коллекции.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Работа с интерфейсами коллекции OM в XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265109"
---
# <a name="working-with-xps-om-collection-interfaces"></a>Работа с интерфейсами коллекции OM в XPS

Описывает, как использовать общие методы интерфейсов коллекции.

## <a name="contents"></a>Содержимое

Методы, описанные в этом разделе, показаны в следующем списке. Не все интерфейсы коллекций поддерживают каждый из этих методов, а некоторые интерфейсы также поддерживают методы, не описанные на этой странице. Список методов, поддерживаемых конкретным интерфейсом, см. в описании этого интерфейса.

<dl>

[Метод Append](#append-method)  
[Метод GetAt](#getat-method)  
[Метод GetCount](#getcount-method)  
[Метод Инсертат](#insertat-method)  
[Метод RemoveAt](#removeat-method)  
[Метод SetAt](#setat-method)  
</dl>

[См. также:](#see-also)

## <a name="append-method"></a>Метод Append

Добавляет объект в конец коллекции.

**Универсальный синтаксис**


```C++
HRESULT Append(
  [in]  Object *object
);
```



**Описание**

В конец коллекции этот метод добавляет объект, который передается в список параметров, как показано на следующей схеме.

![Рисунок, показывающий, как Append добавляет запись в коллекцию](images/generic-append.png)

## <a name="getat-method"></a>Метод GetAt

Возвращает объект из указанного расположения в коллекции.

**Универсальный синтаксис**


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



**Описание**

Записывает объект, хранящийся в расположении коллекции, заданном параметром *index* , в переменную, на которую ссылается *объект*. Это действие не изменяет содержимое коллекции. Этот процесс представлен на схеме ниже.

![Рисунок, показывающий, как GetAt извлекает запись из коллекции.](images/generic-getat.png)

## <a name="getcount-method"></a>Метод GetCount

Возвращает число объектов, хранящихся в коллекции.

**Универсальный синтаксис**


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



**Описание**

Записывает количество объектов, которые в данный момент хранятся в коллекции, в переменную, на которую ссылается *Count*. Это действие не изменяет содержимое коллекции. Этот процесс представлен на схеме ниже.

![фигура, показывающая, как функция NOCOUNT получает количество записей в коллекции](images/generic-getcount.png)

## <a name="insertat-method"></a>Метод Инсертат

Вставляет объект в указанное место коллекции.

**Универсальный синтаксис**


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Описание**

Объект, передаваемый в *объект* , вставляется в коллекцию в расположении, указанном параметром *index*. Перед вставкой нового *объекта* этот метод перемещается на 1 объект, который ранее занимал место в *индексе* , и перемещает все указатели интерфейса после *индекса*. Этот процесс представлен на схеме ниже.

![Рисунок, показывающий, как инсертат добавляет запись в коллекцию](images/generic-insertat.png)

## <a name="removeat-method"></a>Метод RemoveAt

Удаляет объект из указанного расположения в коллекции.

**Универсальный синтаксис**


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



**Описание**

Этот метод освобождает объект из расположения, заданного параметром *index*, а затем сжимает коллекцию, уменьшая на 1 индекс каждого указателя, следующего за *индексом*. Этот процесс представлен на схеме ниже.

![Рисунок, показывающий, как метод RemoveAt удаляет запись из коллекции](images/generic-removeat.png)

## <a name="setat-method"></a>Метод SetAt

Заменяет объект в указанном месте в коллекции.

**Универсальный синтаксис**


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Описание**

Этот метод сначала освобождает объект в расположении, на которое ссылается *индекс*, а затем заменяет этот объект на тот, который передается в *объект*. Этот процесс представлен на схеме ниже.

![Рисунок, показывающий, как SetAt заменяет запись в коллекции](images/generic-setat.png)

## <a name="see-also"></a>См. также:

<dl>

[**икспсомколорпрофилересаурцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[**икспсомдашколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[**икспсомдокументколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[**икспсомфонтресаурцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[**икспсомжеометрифигуреколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[**икспсомградиентстопколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[**икспсомимажересаурцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[**икспсомнамеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[**икспсомпажереференцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[**икспсомпартуриколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[**икспсомремотедиктионариресаурцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[**икспсомсигнатуреблоккресаурцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[**икспсомвисуалколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[**икспссигнатуреблоккколлектион**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[**икспссигнатуреколлектион**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[**икспссигнатуререкуестколлектион**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



