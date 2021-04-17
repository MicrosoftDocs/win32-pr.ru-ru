---
description: 'Выводит список запросов для метода IDirect3DAuthenticatedChannel9:: Query.'
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: Запросы Защита содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a72f7f054783a644cb352727f4bf65864bf5f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710840"
---
# <a name="content-protection-queries"></a>Запросы Защита содержимого

Выводит список запросов для метода [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .



| Запрос состояния                                                                                                                            | Описание                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DAUTHENTICATEDQUERY \_ акцессибилитяттрибутес**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Возвращает тип шины ввода-вывода, используемой для отправки данных в GPU.                                                                                                   |
| [**D3DAUTHENTICATEDQUERY \_ чаннелтипе**](d3dauthenticatedquery-channeltype.md)                                                           | Возвращает тип канала, прошедшего проверку подлинности.                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md)                                                       | Возвращает дескрипторы криптографического сеанса и устройства Direct3D, связанные с указанным устройством декодера DirectX Video Acceleration 2 (ДКСВА-2). |
| [**D3DAUTHENTICATEDQUERY \_ куррентенкриптионвхенакцессибле**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Возвращает тип шифрования, который применяется до того, как содержимое становится доступным для ЦП или шины.                                                            |
| [**D3DAUTHENTICATEDQUERY \_ девицехандле**](d3dauthenticatedquery-devicehandle.md)                                                         | Возвращает маркер устройства, связанного с этим каналом с проверкой подлинности.                                                                          |
| [**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Возвращает один из типов шифрования, который можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.                                     |
| [**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуидкаунт**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Возвращает число типов шифрования, которые можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.                                  |
| [**D3DAUTHENTICATEDQUERY \_ аутпутид**](d3dauthenticatedquery-outputid.md)                                                                 | Возвращает один из идентификаторов вывода, связанный с указанным сеансом шифрования и устройством Direct3D.                                        |
| [**D3DAUTHENTICATEDQUERY \_ аутпутидкаунт**](d3dauthenticatedquery-outputidcount.md)                                                       | Возвращает число идентификаторов вывода, связанных с указанным сеансом шифрования и устройством Direct3D.                                             |
| [**\_Защита D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md)                                                             | Возвращает текущий уровень защиты для устройства.                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесс**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Возвращает сведения о процессе, которому разрешено открывать общие ресурсы с ограниченным доступом.                                                        |
| [**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесскаунт**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Возвращает число процессов, которым разрешено открывать общие ресурсы с ограниченным доступом.                                                           |
| [**D3DAUTHENTICATEDQUERY \_ унрестриктедпротектедшаредресаурцекаунт**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Возвращает количество защищенных общих ресурсов, которые могут быть открыты любым процессом без ограничений.                                                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[API-интерфейсы видео Direct3D](direct3d-video-apis.md)
</dt> <dt>

[Защита содержимого на основе GPU](gpu-based-content-protection.md)
</dt> </dl>

 

 



