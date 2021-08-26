---
title: ILockBytes — реализация глобальной памяти
description: Реализация глобальной памяти ILockBytes реализуется для объекта массива байтов, лежащего в основе объекта хранилища составных файлов COM и предназначенного для чтения и записи непосредственно в глобальной памяти.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Стрктд STG, реализации, глобальная память
- ILockBytes Стрктд STG, реализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f9786f29433bcc02e0b56f3ea9d45c949593f60962e80a650d80ed625da41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867453"
---
# <a name="ilockbytes---global-memory-implementation"></a>ILockBytes — реализация глобальной памяти

Реализация глобальной памяти ILockBytes реализуется для объекта массива байтов, лежащего в основе объекта хранилища составных файлов COM и предназначенного для чтения и записи непосредственно в глобальной памяти.

## <a name="when-to-use"></a>Назначение

Методы [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) вызываются из составных реализаций файлов класса [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) и [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) для объекта хранилища составных файлов, созданного с помощью вызова [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).

## <a name="remarks"></a>Remarks

Ниже приведены методы реализации глобальной памяти [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .

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

В отличие от реализации на основе файлов, вызов этого метода в реализации глобальной памяти не имеет силы.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**
</dt> <dd>

Задает размер массива байтов.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**
</dt> <dd>

Эта реализация не поддерживает блокировку, поэтому *двлоккстипе* имеет значение 0. Вызывающий объект должен обеспечивать допустимые и взаимоисключающие обращения.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**
</dt> <dd>

Эта реализация не поддерживает блокировку.

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**
</dt> <dd>

Реализация метода [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) , предоставляемая моделью COM, вызывает метод [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) для получения данных о объекте массива байтов. Если для массива байтов нет допустимого имени, метод **ILockBytes:: stat** , ПРЕДОСТАВЛЕННЫЙ моделью COM, возвращает **значение NULL** в элемент **пвкснаме** структуры [**статстг**](/windows/win32/api/objidl/ns-objidl-statstg) .

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**Метод IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




