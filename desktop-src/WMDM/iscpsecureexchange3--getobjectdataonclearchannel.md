---
title: Метод Жетобжектдатаонклеарчаннел
description: метод жетобжектдатаонклеарчаннел передает блок данных объекта на открытый канал обратно в Windows диспетчер устройств мультимедиа.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Метод Жетобжектдатаонклеарчаннел Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10e09697653c2ef1235ae9a3ea3a93a45437d1cf45a1f4de72ec99b0812b9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619874"
---
# <a name="getobjectdataonclearchannel-method"></a>Метод Жетобжектдатаонклеарчаннел

метод **жетобжектдатаонклеарчаннел** передает блок данных объекта на открытый канал обратно в Windows диспетчер устройств мультимедиа.

Этот метод идентичен [**искпсекуриксчанже:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , за исключением того, что данные, возвращаемые этим методом, не шифруются. Поэтому этот метод является более эффективным.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* 
</dt> <dd>

Указатель на объект устройства.

</dd> <dt>

*pData* 
</dt> <dd>

Указатель на буфер для приема данных.

</dd> <dt>

*пдвсизе* 
</dt> <dd>

Указатель на **DWORD** , содержащий размер перемещения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. Если метод завершается с ошибкой, возвращается код ошибки **HRESULT** .



| Код возврата                                                                                                | Описание                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Проверка вмдм \_ E \_ Mac \_ не пройдена**</dt> </dl> | Недопустимый код проверки подлинности сообщения.<br/>                                    |
| <dl> <dt>**ВМДМ \_ E \_**</dt> </dl>           | Вызывающий объект не имеет прав, необходимых для выполнения запрошенной операции.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                    | Сбой метода. Прекращение взаимодействия с поставщиком содержимого.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Параметр является недопустимым указателем или **пустым** .<br/>                                   |
| <dl> <dt>**\_Ошибка E**</dt> </dl>                     | Произошла неизвестная ошибка.<br/>                                                   |



 

## <a name="remarks"></a>Remarks

для передачи данных Windows Media диспетчер устройств вызывает метод [трансферконтаинердатаонклеарчаннел](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) для получения данных контейнера. затем вызывается **жетобжектдатаонклеарчаннел** для передачи блоков данных объекта от поставщика содержимого в Windows диспетчер устройств мультимедиа. если \_ параметр S ок возвращается с *пдвсизе* , которому присвоено значение 0, Windows Media диспетчер устройств не запрашивает дальнейшие данные.

Этот метод идентичен [**искпсекуриксчанже:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , за исключением того, что данные, возвращаемые этим методом, не шифруются. Поэтому этот метод является более эффективным.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ВМСКП. idl</dt> </dl>    |
| Библиотека<br/> | <dl> <dt>Мссачлп. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Искпсекуриксчанже:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**Интерфейс ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





