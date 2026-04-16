# must have in your loop

```python
optimizer.zero_grad()
logits = model(x)
loss = criterion(logits, labels)
loss.backward()
optimizer.step()
```

---

# ok now make sure that:

- [ ] .to(device)
- [ ] wired the data in
- [ ] epoch loop
- [ ] validation loop [swith model.eval() and torch.no_grad()!, back to model.train()]
- [ ] loss + metric reported
- [ ] torch.save() <3
