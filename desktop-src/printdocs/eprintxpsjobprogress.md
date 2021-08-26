---
description: Указывает, что в данный момент выполняет диспетчер очереди при обработке задания печати XPS.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: Перечисление Епринткспсжобпрогресс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ef3d72d983388c022afbb0e914f87a17587f70b8e175dd57dabcd61d224e93bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949644"
---
# <a name="eprintxpsjobprogress-enumeration"></a>Перечисление Епринткспсжобпрогресс

Указывает, что в данный момент выполняет диспетчер очереди при обработке задания печати XPS.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**каддингдокументсекуенце**
</dt> <dd>

Последовательность документов собирается добавиться в задание XPS.

</dd> <dt>

<span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**кдокументсекуенцеаддед**
</dt> <dd>

В задание XPS добавлена последовательность документов.

</dd> <dt>

<span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**каддингфикседдокумент**
</dt> <dd>

Фиксированный документ будет добавлен в задание XPS.

</dd> <dt>

<span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**кфикседдокументаддед**
</dt> <dd>

К заданию XPS добавлен фиксированный документ.

</dd> <dt>

<span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**каддингфикседпаже**
</dt> <dd>

Страница собирается добавиться в задание XPS.

</dd> <dt>

<span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**кфикседпажеаддед**
</dt> <dd>

В задание XPS добавлена страница.

</dd> <dt>

<span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**кресаурцеаддед**
</dt> <dd>

Ресурс был добавлен в задание XPS.

</dd> <dt>

<span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**кфонтаддед**
</dt> <dd>

В задание XPS добавлен шрифт.

</dd> <dt>

<span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**кимажеаддед**
</dt> <dd>

В задание XPS Добавлено изображение.

</dd> <dt>

<span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**ккспсдокументкоммиттед**
</dt> <dd>

Данные для задания XPS были зафиксированы.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это перечисление в основном используется в качестве параметра функции [**репортжобпроцессингпрогресс**](reportjobprocessingprogress.md) .

Эти значения могут быть связаны либо с очередью печати, либо с фазой отрисовки задания печати.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |



 

 




