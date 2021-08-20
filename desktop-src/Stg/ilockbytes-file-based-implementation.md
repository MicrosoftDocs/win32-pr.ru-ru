---
title: Реализация ILockBytes-File-Based
description: Реализуется для объекта массива байтов, лежащего в основе объекта хранилища составных файлов COM и предназначенного для чтения и записи непосредственно в файл на диске.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Стрктд STG, реализации, на основе файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3dcfd11562f6a023d1f77af44b51ff7016cb61afdb16f2e4d72f81114fc132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961813"
---
# <a name="ilockbytes---file-based-implementation"></a>Реализация ILockBytes-File-Based

Реализуется для объекта массива байтов, лежащего в основе объекта хранилища составных файлов COM и предназначенного для чтения и записи непосредственно в файл на диске.

## <a name="when-to-use"></a>Назначение

Методы [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) вызываются из составных реализаций файлов класса [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) и [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) для объекта хранилища составных файлов, созданного с помощью вызова [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), поэтому вам не нужно вызывать их напрямую.

## <a name="remarks"></a>Remarks

Ниже приведены методы реализации File-Based [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: Реадат**
</dt> <dd>

Считывает блок байтов из указанного смещения в начале массива байтов.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: Вритеат**
</dt> <dd>

Записывает блок байтов из указанного смещения в начале массива байтов.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**
</dt> <dd>

Гарантирует, что все внутренние буферы, поддерживаемые реализацией [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) , записываются в базовое физическое хранилище.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**
</dt> <dd>

Задает размер массива байтов.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**
</dt> <dd>

Параметр *двлокктипес* имеет значение Lock \_ онлйонце или Lock \_ монопольно, что разрешает или ограничивает доступ к заблокированным регионам.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**
</dt> <dd>

Этот метод разблокирует область, Заблокированную [**ILockBytes:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**
</dt> <dd>

Реализация метода [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) , предоставляемая моделью COM, вызывает метод [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) для получения сведений о объекте массива байтов. Если для массива байтов нет допустимого имени, метод **ILockBytes:: stat** , ПРЕДОСТАВЛЕННЫЙ моделью COM, возвращает **значение NULL** в элемент **пвкснаме** структуры [**статстг**](/windows/win32/api/objidl/ns-objidl-statstg) .

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**Метод IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




