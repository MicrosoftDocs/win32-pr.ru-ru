---
description: Указывает, будет ли приемник мультимедиа ASF автоматически корректировать скорость потока.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: Свойство MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9c026010ba1995bb15f37562eb378361051e4f9f8da4eb9e065dfadfdccb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690551"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a>\_Свойство мфпкэй асфмедиасинк \_ АВТОнастройки скорости \_

Указывает, будет ли приемник мультимедиа ASF автоматически корректировать скорость потока.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**VARIANT \_ bool**

Логическое значение VT \_

**булвал**



## <a name="remarks"></a>Remarks

Если значение этого свойства равно \_ true, приемник мультимедиа ASF автоматически корректирует скорость передачи содержимого ASF в ответ на характеристики мультиплексированных потоков.

Это свойство влияет на работу приемника мультимедиа ASF, когда поток переполняет параметры "сегмент утечки" приемника:



| Значение              | Поведение                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **ВАРИАНТ \_ true**  | Приемник мультимедиа ASF автоматически корректирует скорость передачи содержимого ASF в ответ на характеристики мультиплексирования потоков. |
| **ВАРИАНТ \_ false** | Приемник мультимедиа ASF использует значение скорости потока, предоставленное приложением.                                                                |



 

Значение по умолчанию — **Variant \_ false**.

Задайте это свойство при настройке приемника мультимедиа ASF. Использование зависит от того, какая функция вызывается для создания приемника мультимедиа ASF:

-   [**Мфкреатеасфмедиасинк**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): запросите полученный указатель [**Имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) для интерфейса **ипропертисторе** .

-   [**Мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): вызов [**Имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) в указателе [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , указанном в параметре *pContentInfo* .

Если задать для этого свойства значение "VARIANT true", \_ приемник мультимедиа ASF должен установить флаг **\_ \_ авторегулировки \_ скорости мфасф мультиплексора** в мультиплексоре ASF. См. раздел [**имфасфмултиплексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).

дополнительные сведения о концепции сегмента утечки см. в разделе "модель буфера с утечкой данных" в документации по пакету SDK Windows Media Format.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[**MF \_ асфстреамконфиг \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




