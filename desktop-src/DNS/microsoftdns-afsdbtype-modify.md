---
title: Метод Modify класса MicrosoftDNS_AFSDBType
description: Метод Modify обновляет запись ресурса сервера базы данных файловой системы AFS (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_AFSDBType класс
- MicrosoftDNS_AFSDBType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654494"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a>Метод Modify \_ класса микрософтднс афсдбтипе

Метод **Modify** обновляет запись ресурса сервера базы данных файловой системы AFS (AFSDB).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Подтип* \[ в необязательное\]
</dt> <dd>

Подтип ведущего сервера AFS. Для подтипа 1 (значение 1) на узле имеется сервер AFS версии 3,0 для именованной ячейки AFS. В случае подтипа 2 (значение = 2) узел имеет прошедший проверку подлинности сервер имен, в котором размещен узел корневого каталога ячеек для именованной ячейки DCE/NCA.

</dd> <dt>

*Имя сервера* \[ в необязательное\]
</dt> <dd>

Полное доменное имя, указывающее узел с сервером для ячейки AFS, указанной в имени владельца.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Ссылка на измененный объект.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Любой параметр, не указанный, остается неизменным в измененной записи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Микрософтднс \_ афсдбтипе**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Афсдбтипе микрософтднс**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





