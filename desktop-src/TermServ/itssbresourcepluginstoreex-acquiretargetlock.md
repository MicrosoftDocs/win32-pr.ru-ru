---
title: Итссбресаурцеплугинсторикс Аккуиретаржетлокк, метод
description: Блокирует целевой объект.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аккуиретаржетлокк
- Службы удаленных рабочих столов метода Аккуиретаржетлокк, интерфейс Итссбресаурцеплугинсторикс
- Службы удаленных рабочих столов интерфейса Итссбресаурцеплугинсторикс, метод Аккуиретаржетлокк
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80a2ab7068ec754a89e384028f2d43989345e9801c4ededb800117d211b0f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128461"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>Метод Итссбресаурцеплугинсторикс:: Аккуиретаржетлокк

Блокирует целевой объект.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*TargetName* \[ окне\]
</dt> <dd>

Имя целевого объекта для блокировки.

</dd> <dt>

*двтимеаут* \[ окне\]
</dt> <dd>

Время ожидания для операции в миллисекундах.

</dd> <dt>

*ппконтекст* \[ заполняет\]
</dt> <dd>

Возвращает указатель на контекст блокировки. Чтобы снять блокировку, укажите этот указатель на метод [**релеасетаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

После получения блокировки предполагается, что вызывающий поток имеет монопольный доступ к целевому объекту и, следовательно, ни один другой поток (на том же компьютере) не сможет его обновить. Поэтому вызывающий поток должен вызвать метод [**релеасетаржетлокк**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) , как только он внес необходимые обновления в целевой объект.

> [!IMPORTANT]
> Эта блокировка не полностью мешает изменению целевых объектов извне, если в развертывании существует несколько посредников подключений. Вызывающий поток должен быть подготовлен для корректной обработки ошибки и повторного выполнения целевого обновления.

 

этот метод доступен в Windows Server 2012 R2 с [KB3091411](https://support.microsoft.com/kb/3091411) , установленным в интерфейсе [**итссбресаурцеплугинсторикс**](itssbresourcepluginstoreex.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                             |
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                                                             |
| IDL<br/>                      | <dl> <dt>Сбтсв. idl</dt> </dl>          |
| IID<br/>                      | IID \_ итссбресаурцеплугинсторикс определен как 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**итссбресаурцеплугинсторикс**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





